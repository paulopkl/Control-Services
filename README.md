# Control-Services
this project was developed during the Week-SpringRest-Api of AlgaWorks.

<h1>this project is an API that follows Rest standards. Use it for your Company/Startup that needs a service order control system.</h1>

<p>you just need to download osWorks_paulopkljk-0.0.1-SNAPSHOT.jar</p>

# URI's:
<h4>Client</h4>
<table>
    <thead>
        <th>Title</th>
        <th>Usage</th>
        <th>Method</th>
    </thead>
    <tbody>
        <tr>
            <td>Add Client</td>
            <td>http://localhost:8080/clientes</td>
            <td>POST</td>
        </tr>
        <tr>
            <td>Search Client</td>
            <td>http://localhost:8080/clientes/{ClientId}</td>
            <td>GET</td>
        </tr>
        <tr>
            <td>List Client</td>
            <td>http://localhost:8080/clientes</td>
            <td>GET</td>
        </tr>
        <tr>
            <td>Update Client</td>
            <td>http://localhost:8080/clientes/{ClientId}</td>
            <td>PUT</td>
        </tr>
        <tr>
            <td>Delete Client</td>
            <td>http://localhost:8080/clientes/{ClientId}</td>
            <td>DELETE</td>
        </tr>
    </tbody>
</table>

<h4>Service Orders, Comments</h4>
<table>
    <thead>
        <th>Title</th>
        <th>Usage</th>
        <th>Method</th>
    </thead>
    <tbody>
        <tr>
            <td>Add - Service-Order</td>
            <td>http://localhost:8080/ordens-servico</td>
            <td>POST</td>
        </tr>
        <tr>
            <td>Finish - Service-Order</td>
            <td>http://localhost:8080/ordens-servico/{ServiceOrderId}/finalizacao</td>
            <td>PUT</td>
        </tr>
        <tr>
            <td>List Service-Orders</td>
            <td>http://localhost:8080/ordens-servico</td>
            <td>GET</td>
        </tr>
        <tr>
            <td>Search - Service-Order</td>
            <td>http://localhost:8080/ordens-servico/{ServiceOrderId}</td>
            <td>GET</td>
        </tr>
        <tr>
            <td>List Comments</td>
            <td>http://localhost:8080/ordens-servico/{ServiceOrderId}/comentarios</td>
            <td>GET</td>
        </tr>
        <tr>
            <td>Add - Comment</td>
            <td>http://localhost:8080/ordens-servico/{ServiceOrderId}/comentarios</td>
            <td>POST</td>
        </tr>
    </tbody>
</table>

<h4>Add - Client | POST</h4>
<p>Request Body:</p>

{
    "nome": "[Client - Name]",
    "email": "[Client - Email]",
    "telefone": "[Client - Phone]"
}

<h4>Update Client | PUT</h4>
<p>Request Body:</p>

{
    "nome": "[Client - Name]",
    "email": "[Client - Email]",
    "telefone": "[Client - Phone]"
}

<h4>Add - Service-Order</h4>
<p>Request Body:</p>

{
    "cliente": {
        "id": [Client Id]
    },
    "descricao": "[Description. max: 255 letters]",
    "preco": [Value]
}

<h4>Add - Comment</h4>
<p>Request Body</p>

{
    "descricao": "[Message - Description. max: 255 letters]"
}