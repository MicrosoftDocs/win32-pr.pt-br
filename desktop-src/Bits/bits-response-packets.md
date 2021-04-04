---
title: Pacotes de resposta do BITS
description: Pacotes de resposta do BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822302"
---
# <a name="bits-response-packets"></a><span data-ttu-id="6ebc9-103">Pacotes de resposta do BITS</span><span class="sxs-lookup"><span data-stu-id="6ebc9-103">BITS Response Packets</span></span>

<span data-ttu-id="6ebc9-104">A tabela a seguir lista os pacotes de resposta enviados para o cliente BITS para trabalhos de upload e upload-reply.</span><span class="sxs-lookup"><span data-stu-id="6ebc9-104">The following table lists the response packets sent to the BITS client for upload and upload-reply jobs.</span></span> <span data-ttu-id="6ebc9-105">A tabela lista os pacotes na sequência típica que eles são enviados para o cliente.</span><span class="sxs-lookup"><span data-stu-id="6ebc9-105">The table lists the packets in the typical sequence they are sent to the client.</span></span>



| <span data-ttu-id="6ebc9-106">Pacote de resposta</span><span class="sxs-lookup"><span data-stu-id="6ebc9-106">Response packet</span></span>                                      | <span data-ttu-id="6ebc9-107">Finalidade</span><span class="sxs-lookup"><span data-stu-id="6ebc9-107">Purpose</span></span>                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ebc9-108">ACK para ping</span><span class="sxs-lookup"><span data-stu-id="6ebc9-108">Ack for Ping</span></span>](ack-for-ping.md)                     | <span data-ttu-id="6ebc9-109">Reconhece a solicitação de [ping](ping.md) .</span><span class="sxs-lookup"><span data-stu-id="6ebc9-109">Acknowledges the [Ping](ping.md) request.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="6ebc9-110">ACK para Create-Session</span><span class="sxs-lookup"><span data-stu-id="6ebc9-110">Ack for Create-Session</span></span>](ack-for-create-session.md) | <span data-ttu-id="6ebc9-111">Reconhece a solicitação de [criação de sessão](create-session.md) e retorna um identificador de sessão que o cliente bits usa em todas as solicitações subsequentes para identificar essa sessão de transferência de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6ebc9-111">Acknowledges the [Create-Session](create-session.md) request and returns a session identifier that the BITS client uses on all subsequent requests to identify this file transfer session.</span></span> |
| [<span data-ttu-id="6ebc9-112">Confirmação para fragmento</span><span class="sxs-lookup"><span data-stu-id="6ebc9-112">Ack for Fragment</span></span>](ack-for-fragment.md)             | <span data-ttu-id="6ebc9-113">Reconhece a solicitação de [fragmento](fragment.md) e grava o fragmento no arquivo de carregamento no servidor.</span><span class="sxs-lookup"><span data-stu-id="6ebc9-113">Acknowledges the [Fragment](fragment.md) request and writes the fragment to the upload file on the server.</span></span>                                                                                 |
| [<span data-ttu-id="6ebc9-114">ACK para fechamento de sessão</span><span class="sxs-lookup"><span data-stu-id="6ebc9-114">Ack for Close-Session</span></span>](ack-for-close-session.md)   | <span data-ttu-id="6ebc9-115">Reconhece a solicitação de [fechamento de sessão](close-session.md) e libera todos os recursos associados à sessão.</span><span class="sxs-lookup"><span data-stu-id="6ebc9-115">Acknowledges the [Close-Session](close-session.md) request and releases all resources associated with the session.</span></span>                                                                         |
| [<span data-ttu-id="6ebc9-116">ACK para cancelamento de sessão</span><span class="sxs-lookup"><span data-stu-id="6ebc9-116">Ack for Cancel-Session</span></span>](ack-for-cancel-session.md) | <span data-ttu-id="6ebc9-117">Reconhece a solicitação de [cancelamento de sessão](cancel-session.md) e libera todos os recursos associados à sessão.</span><span class="sxs-lookup"><span data-stu-id="6ebc9-117">Acknowledges the [Cancel-Session](cancel-session.md) request and releases all resources associated with the session.</span></span>                                                                       |



 

 

 




