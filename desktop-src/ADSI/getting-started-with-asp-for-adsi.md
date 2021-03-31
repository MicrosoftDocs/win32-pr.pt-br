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
# <a name="getting-started-with-asp-for-adsi"></a><span data-ttu-id="f3598-107">Introdução com ASP para ADSI</span><span class="sxs-lookup"><span data-stu-id="f3598-107">Getting Started with ASP for ADSI</span></span>

<span data-ttu-id="f3598-108">A ADSI pode ser usada para acessar dados de diretório usando uma página ASP.</span><span class="sxs-lookup"><span data-stu-id="f3598-108">ADSI can be used to access directory data using an ASP page.</span></span> <span data-ttu-id="f3598-109">Isso pode ser uma maneira conveniente de executar tarefas de administração e consultas de uma página da Web ou fornecer informações aos funcionários de uma intranet.</span><span class="sxs-lookup"><span data-stu-id="f3598-109">This can be a convenient way to run administration tasks and queries from a webpage or provide information to employees on an intranet.</span></span>

<span data-ttu-id="f3598-110">Uma vantagem de usar o ADSI com ASP é que você pode criar uma experiência de usuário mais rica, pois você pode usar Visual Basic para criar um aplicativo ADSI e oferecê-lo a um usuário por meio de uma página da Web padrão.</span><span class="sxs-lookup"><span data-stu-id="f3598-110">One advantage of using ADSI with ASP is that you can create a richer user experience because you can use Visual Basic to create an ADSI application and offer it to a user through a standard webpage.</span></span> <span data-ttu-id="f3598-111">Por exemplo, você pode criar uma página da Web que permite aos funcionários inserir o sobrenome de um funcionário e retornar um número de telefone para esse funcionário ou criar um formulário que permita aos funcionários atualizar informações pessoais em um banco de dados de recursos humanos da empresa.</span><span class="sxs-lookup"><span data-stu-id="f3598-111">For example, you could create a webpage that enables employees to enter the last name of an employee and get back a phone number for that employee, or create a form that allows employees to update personal information in a company human resources database.</span></span>

<span data-ttu-id="f3598-112">O código ASP começa com ' <% ' e termina com '% > '.</span><span class="sxs-lookup"><span data-stu-id="f3598-112">ASP code starts with '<%' and ends with '%>'.</span></span> <span data-ttu-id="f3598-113">Você pode adicionar código ADSI como VBScript ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f3598-113">You can add ADSI code as VBScript or Visual Basic.</span></span>

<span data-ttu-id="f3598-114">Para criar uma página ASP, você pode usar um editor de página da Web, bloco de notas ou outro editor de texto, ou o sistema de desenvolvimento Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="f3598-114">To create an ASP page, you can use a webpage editor, Notepad or other text editor, or the Microsoft Visual Studio .NET development system.</span></span>

<span data-ttu-id="f3598-115">Antes de executar sua página ASP, configure seu aplicativo ou servidor IIS de acordo com as instruções encontradas em [problemas de autenticação para ADSI com ASP](authentication-issues-for-adsi-with-asp.md).</span><span class="sxs-lookup"><span data-stu-id="f3598-115">Before you run your ASP page, set up your application or IIS server according to the instructions found in [Authentication Issues for ADSI with ASP](authentication-issues-for-adsi-with-asp.md).</span></span>

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a><span data-ttu-id="f3598-116">Um exemplo simples de ASP: Enumerando objetos em um contêiner</span><span class="sxs-lookup"><span data-stu-id="f3598-116">A Simple ASP Sample: Enumerating Objects in a Container</span></span>

<span data-ttu-id="f3598-117">Usando um editor de página da Web, crie uma nova página HTML que aceita o nome distinto de um objeto de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f3598-117">Using a webpage editor, create a new html page which accepts the distinguished name of a container object.</span></span> <span data-ttu-id="f3598-118">Insira o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3598-118">Enter the following code example.</span></span>


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



<span data-ttu-id="f3598-119">Essa página agora pode aceitar um nome de contêiner que é passado para ele e usar ADSI para enumerar objetos no contêiner.</span><span class="sxs-lookup"><span data-stu-id="f3598-119">This page can now accept a container name that is passed to it and use ADSI to enumerate objects in the container.</span></span>

<span data-ttu-id="f3598-120">Crie uma nova página ASP chamada enum. asp e insira o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3598-120">Create a new ASP page called Enum.asp and enter the following code example.</span></span> <span data-ttu-id="f3598-121">Salve esta página na raiz do servidor Web local.</span><span class="sxs-lookup"><span data-stu-id="f3598-121">Save this page at the root of the local web server.</span></span>


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



 

 




