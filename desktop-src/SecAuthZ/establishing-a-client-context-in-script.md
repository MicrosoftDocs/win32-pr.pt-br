---
description: Para estabelecer um contexto de cliente no script, um aplicativo pode criar um contexto de cliente com um identificador para um token, um domínio e um nome de usuário ou uma representação de cadeia de caracteres do identificador de segurança do cliente.
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: Estabelecendo um contexto de cliente no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63c0381834a42d10a03b02ee949f8fe4bf7560bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829441"
---
# <a name="establishing-a-client-context-in-script"></a><span data-ttu-id="9951a-103">Estabelecendo um contexto de cliente no script</span><span class="sxs-lookup"><span data-stu-id="9951a-103">Establishing a Client Context in Script</span></span>

<span data-ttu-id="9951a-104">No Gerenciador de autorização, um aplicativo determina se um cliente recebe acesso a uma operação chamando o método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de um objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , que representa um contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="9951a-104">In Authorization Manager, an application determines whether a client is given access to an operation by calling the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object, which represents a client context.</span></span>

<span data-ttu-id="9951a-105">Um aplicativo pode criar um contexto de cliente com um identificador para um token, um domínio e um nome de usuário ou uma representação de cadeia de caracteres do Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) do cliente.</span><span class="sxs-lookup"><span data-stu-id="9951a-105">An application can create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span>

<span data-ttu-id="9951a-106">Use os métodos [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)e [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) de um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) para criar um contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="9951a-106">Use the [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname), and [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) methods of an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object to create a client context.</span></span>

<span data-ttu-id="9951a-107">O exemplo a seguir mostra como criar um objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) a partir de um nome de cliente.</span><span class="sxs-lookup"><span data-stu-id="9951a-107">The following example shows how to create an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object from a client name.</span></span> <span data-ttu-id="9951a-108">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C e que esse repositório contenha um aplicativo chamado despesas.</span><span class="sxs-lookup"><span data-stu-id="9951a-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense.</span></span>


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

%>
```



 

 
