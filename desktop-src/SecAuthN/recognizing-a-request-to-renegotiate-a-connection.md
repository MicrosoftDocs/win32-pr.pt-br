---
description: A função DecryptMessage (geral) intercepta solicitações de renegociação proveniente do remetente da mensagem. Ele notifica seu aplicativo descriptografando os dados da mensagem e retornando o \_ valor s I \_ renegotiate.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Reconhecendo uma solicitação para renegociar uma conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010982"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a><span data-ttu-id="044e6-104">Reconhecendo uma solicitação para renegociar uma conexão</span><span class="sxs-lookup"><span data-stu-id="044e6-104">Recognizing a Request to Renegotiate a Connection</span></span>

<span data-ttu-id="044e6-105">A função [**DecryptMessage (geral)**](decryptmessage--general.md) intercepta solicitações de renegociação proveniente do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="044e6-105">The [**DecryptMessage (General)**](decryptmessage--general.md) function traps requests for renegotiation coming from the message sender.</span></span> <span data-ttu-id="044e6-106">Ele notifica seu aplicativo descriptografando os dados da mensagem e retornando o \_ valor s I \_ renegotiate.</span><span class="sxs-lookup"><span data-stu-id="044e6-106">It notifies your application by decrypting the message data and returning the SEC\_I\_RENEGOTIATE value.</span></span>

<span data-ttu-id="044e6-107">Seu aplicativo deve lidar com essas solicitações chamando [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) (servidores) ou [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) (clientes) e passando o conteúdo de SECBUFFER_EXTRA retornado de DecryptMessage no SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="044e6-107">Your application must handle such requests by calling [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (servers) or [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) and passing the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="044e6-108">Depois que essa chamada inicial retorna um valor, continue como se seu aplicativo estivesse criando uma nova conexão.</span><span class="sxs-lookup"><span data-stu-id="044e6-108">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 



