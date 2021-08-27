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
ms.openlocfilehash: 05a8ea51efa427c83e78c35806175712b3c6d0d66e0987909f98e23a081415e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913732"
---
# <a name="establishing-a-client-context-in-script"></a>Estabelecendo um contexto de cliente no script

No Gerenciador de autorização, um aplicativo determina se um cliente recebe acesso a uma operação chamando o método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de um objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , que representa um contexto de cliente.

Um aplicativo pode criar um contexto de cliente com um identificador para um token, um domínio e um nome de usuário ou uma representação de cadeia de caracteres do Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) do cliente.

Use os métodos [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)e [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) de um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) para criar um contexto de cliente.

O exemplo a seguir mostra como criar um objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) a partir de um nome de cliente. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C e que esse repositório contenha um aplicativo chamado despesas.


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



 

 
