---
description: Alguns protocolos exigem várias mensagens de autenticação.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuação do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827765"
---
# <a name="client-continuation"></a><span data-ttu-id="3f6f0-103">Continuação do cliente</span><span class="sxs-lookup"><span data-stu-id="3f6f0-103">Client Continuation</span></span>

<span data-ttu-id="3f6f0-104">Alguns protocolos exigem várias mensagens de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3f6f0-104">Some protocols require multiple authentication messages.</span></span> <span data-ttu-id="3f6f0-105">Nesse caso, o cliente analisa a resposta do servidor e chama [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) novamente usando o status de continuação da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="3f6f0-105">In this case, the client parses the response from the server and calls [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) again using the continue status from the previous call.</span></span> <span data-ttu-id="3f6f0-106">O cliente verifica o status de retorno dessa chamada e pode ser necessário para continuar para os segmentos adicionais.</span><span class="sxs-lookup"><span data-stu-id="3f6f0-106">The client checks the return status from this call and might be required to continue for additional legs.</span></span> <span data-ttu-id="3f6f0-107">Ele usa as informações em *pOutput* para construir uma mensagem e a envia para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3f6f0-107">It uses the information in *pOutput* to construct a message and sends it to the server.</span></span>

 

 
