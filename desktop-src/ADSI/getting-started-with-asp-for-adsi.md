---
title: Introdução com ASP para ADSI
description: A ADSI pode ser usada para acessar dados de diretório usando uma página ASP. Isso pode ser uma maneira conveniente de executar tarefas de administração e consultas de uma página da Web ou fornecer informações aos funcionários de uma intranet.
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ADSI ASP
- ADSI, páginas ASP
- ADSI, páginas ASP, exemplo de código ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634875"
---
# <a name="getting-started-with-asp-for-adsi"></a>Introdução com ASP para ADSI

A ADSI pode ser usada para acessar dados de diretório usando uma página ASP. Isso pode ser uma maneira conveniente de executar tarefas de administração e consultas de uma página da Web ou fornecer informações aos funcionários de uma intranet.

Uma vantagem de usar o ADSI com ASP é que você pode criar uma experiência de usuário mais rica, pois você pode usar Visual Basic para criar um aplicativo ADSI e oferecê-lo a um usuário por meio de uma página da Web padrão. Por exemplo, você pode criar uma página da Web que permite aos funcionários inserir o sobrenome de um funcionário e retornar um número de telefone para esse funcionário ou criar um formulário que permita aos funcionários atualizar informações pessoais em um banco de dados de recursos humanos da empresa.

O código ASP começa com ' <% ' e termina com '% > '. Você pode adicionar código ADSI como VBScript ou Visual Basic.

Para criar uma página ASP, você pode usar um editor de página da Web, bloco de notas ou outro editor de texto, ou o sistema de desenvolvimento Microsoft Visual Studio .NET.

Antes de executar sua página ASP, configure seu aplicativo ou servidor IIS de acordo com as instruções encontradas em [problemas de autenticação para ADSI com ASP](authentication-issues-for-adsi-with-asp.md).

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a>Um exemplo simples de ASP: Enumerando objetos em um contêiner

Usando um editor de página da Web, crie uma nova página HTML que aceita o nome distinto de um objeto de contêiner. Insira o exemplo de código a seguir.


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



Essa página agora pode aceitar um nome de contêiner que é passado para ele e usar ADSI para enumerar objetos no contêiner.

Crie uma nova página ASP chamada enum. asp e insira o exemplo de código a seguir. Salve esta página na raiz do servidor Web local.


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 




