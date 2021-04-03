---
title: Pacotes de solicitação do BITS
description: Pacotes de solicitação do BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916021"
---
# <a name="bits-request-packets"></a><span data-ttu-id="09ed8-103">Pacotes de solicitação do BITS</span><span class="sxs-lookup"><span data-stu-id="09ed8-103">BITS Request Packets</span></span>

<span data-ttu-id="09ed8-104">Pacotes de solicitação descrevem solicitações de cliente.</span><span class="sxs-lookup"><span data-stu-id="09ed8-104">Request packets describe client requests.</span></span> <span data-ttu-id="09ed8-105">Pode haver apenas uma solicitação pendente em um determinado momento; Você deve receber um [ACK](bits-response-packets.md) para a solicitação atual do servidor antes de enviar outra solicitação.</span><span class="sxs-lookup"><span data-stu-id="09ed8-105">There can be only one outstanding request at any given time; you must receive an [Ack](bits-response-packets.md) for the current request from the server before sending another request.</span></span>

<span data-ttu-id="09ed8-106">A tabela a seguir lista os pacotes de solicitação enviados ao servidor BITS para trabalhos de upload e de resposta de upload.</span><span class="sxs-lookup"><span data-stu-id="09ed8-106">The following table lists the request packets sent to the BITS server for upload and upload-reply jobs.</span></span> <span data-ttu-id="09ed8-107">A tabela lista os pacotes na sequência típica que eles são enviados para o servidor.</span><span class="sxs-lookup"><span data-stu-id="09ed8-107">The table lists the packets in the typical sequence they are sent to the server.</span></span>



| <span data-ttu-id="09ed8-108">Pacote de solicitação</span><span class="sxs-lookup"><span data-stu-id="09ed8-108">Request packet</span></span>                       | <span data-ttu-id="09ed8-109">Finalidade</span><span class="sxs-lookup"><span data-stu-id="09ed8-109">Purpose</span></span>                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09ed8-110">Executar</span><span class="sxs-lookup"><span data-stu-id="09ed8-110">Ping</span></span>](ping.md)                     | <span data-ttu-id="09ed8-111">Estabelece uma conexão e negocia a segurança com o servidor.</span><span class="sxs-lookup"><span data-stu-id="09ed8-111">Establishes a connection and negotiates security with the server.</span></span>                                                                                              |
| [<span data-ttu-id="09ed8-112">Criar sessão</span><span class="sxs-lookup"><span data-stu-id="09ed8-112">Create-Session</span></span>](create-session.md) | <span data-ttu-id="09ed8-113">Solicita uma sessão de carregamento com o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="09ed8-113">Requests an upload session with the BITS server.</span></span>                                                                                                               |
| [<span data-ttu-id="09ed8-114">Fragmento</span><span class="sxs-lookup"><span data-stu-id="09ed8-114">Fragment</span></span>](fragment.md)             | <span data-ttu-id="09ed8-115">Envia um fragmento do arquivo para o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="09ed8-115">Sends a fragment of the file to the BITS server.</span></span> <span data-ttu-id="09ed8-116">O número de solicitações de fragmento enviadas depende do tamanho do fragmento escolhido e do tamanho do arquivo de carregamento.</span><span class="sxs-lookup"><span data-stu-id="09ed8-116">The number of fragment requests sent depends on the fragment size you choose and the size of the upload file.</span></span> |
| [<span data-ttu-id="09ed8-117">Fechar sessão</span><span class="sxs-lookup"><span data-stu-id="09ed8-117">Close-Session</span></span>](close-session.md)   | <span data-ttu-id="09ed8-118">Encerra a sessão de carregamento de arquivo com o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="09ed8-118">Ends the file upload session with the BITS server.</span></span>                                                                                                             |
| [<span data-ttu-id="09ed8-119">Cancelar sessão</span><span class="sxs-lookup"><span data-stu-id="09ed8-119">Cancel-Session</span></span>](cancel-session.md) | <span data-ttu-id="09ed8-120">Encerra a sessão de carregamento de arquivo com o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="09ed8-120">Ends the file upload session with the BITS server.</span></span> <span data-ttu-id="09ed8-121">Normalmente, você envia o pacote Cancel-Session se o usuário cancelou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="09ed8-121">Typically, you send the Cancel-Session packet if the user canceled the job.</span></span>                                 |



 

<span data-ttu-id="09ed8-122">O pacote de ping é opcional.</span><span class="sxs-lookup"><span data-stu-id="09ed8-122">The Ping packet is optional.</span></span> <span data-ttu-id="09ed8-123">Em vez de enviar um pacote de ping, você pode usar o pacote Create-Session para estabelecer uma conexão e negociar a segurança.</span><span class="sxs-lookup"><span data-stu-id="09ed8-123">Instead of sending a Ping packet, you can use the Create-Session packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="09ed8-124">No entanto, é mais eficiente usar o pacote de ping para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="09ed8-124">However, it is more efficient to use the Ping packet for this purpose.</span></span>

 

 




