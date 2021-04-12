---
description: Descreve o processo de uma operação de e/s de rede no Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descrição de uma operação de e/s de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296809"
---
# <a name="description-of-a-network-io-operation"></a><span data-ttu-id="9178f-103">Descrição de uma operação de e/s de rede</span><span class="sxs-lookup"><span data-stu-id="9178f-103">Description of a Network I/O Operation</span></span>

<span data-ttu-id="9178f-104">A figura a seguir ilustra o processo de uma operação de e/s de rede no Windows.</span><span class="sxs-lookup"><span data-stu-id="9178f-104">The following figure illustrates the process of a network I/O operation under Windows.</span></span>

![operação de e/s de rede no Windows](images/fig4.png)

<span data-ttu-id="9178f-106">Quando um aplicativo chama uma função de e/s de arquivo para acessar um arquivo em um computador remoto, ocorrem os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="9178f-106">When an application calls a file I/O function to access a file on a remote computer, the following events occur:</span></span>

-   <span data-ttu-id="9178f-107">A solicitação de e/s é interceptada por um [redirecionador de rede](network-redirectors.md), também chamado simplesmente de redirecionador, no computador local.</span><span class="sxs-lookup"><span data-stu-id="9178f-107">The I/O request is intercepted by a [network redirector](network-redirectors.md), also referred to simply as a redirector, on the local computer.</span></span> <span data-ttu-id="9178f-108">Isso é descrito na figura anterior pela seta sólida entre o aplicativo e o redirecionador do cliente.</span><span class="sxs-lookup"><span data-stu-id="9178f-108">This is depicted in the preceding figure by the solid arrow between the application and the client redirector.</span></span>
-   <span data-ttu-id="9178f-109">O redirecionador constrói um pacote de dados que contém todas as informações sobre a solicitação e a envia para o servidor onde o arquivo está localizado.</span><span class="sxs-lookup"><span data-stu-id="9178f-109">The redirector constructs a data packet containing all of the information about the request, and sends it to the server where the file is located.</span></span> <span data-ttu-id="9178f-110">Isso é descrito na figura anterior pela seta sólida entre o redirecionador do cliente e o redirecionador do servidor.</span><span class="sxs-lookup"><span data-stu-id="9178f-110">This is depicted in the preceding figure by the solid arrow between the client redirector and the server redirector.</span></span>
-   <span data-ttu-id="9178f-111">O redirecionador no servidor recebe o pacote do cliente, autentica o acesso ao arquivo exigido pela solicitação de e/s e, se autenticado, executa a solicitação em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="9178f-111">The redirector on the server receives the packet from the client, authenticates the access to the file required by the I/O request, and, if authenticated, executes the request on behalf of the client.</span></span> <span data-ttu-id="9178f-112">Caso contrário, ele retorna um código de erro para o redirecionador no cliente.</span><span class="sxs-lookup"><span data-stu-id="9178f-112">If not, it returns an error code to the redirector on the client.</span></span> <span data-ttu-id="9178f-113">Isso é representado na figura anterior pela seta sólida curvada entre o redirecionador do servidor e o arquivo.</span><span class="sxs-lookup"><span data-stu-id="9178f-113">This is depicted in the preceding figure by the curved solid arrow between the server redirector and the file.</span></span>
-   <span data-ttu-id="9178f-114">Quando a solicitação é executada, o redirecionador no servidor envia todos os dados resultantes da solicitação de e/s para o redirecionador no cliente, juntamente com uma notificação de êxito.</span><span class="sxs-lookup"><span data-stu-id="9178f-114">When the request has been executed, the redirector on the server sends any data resulting from the I/O request to the redirector on the client along with a success notification.</span></span> <span data-ttu-id="9178f-115">Isso é descrito na figura anterior pela seta pontilhada entre o servidor e o redirecionador do cliente.</span><span class="sxs-lookup"><span data-stu-id="9178f-115">This is depicted in the preceding figure by the dotted arrow between the server and the client redirector.</span></span>
-   <span data-ttu-id="9178f-116">O redirecionador no cliente recebe o pacote do servidor e passa os dados no pacote para o aplicativo junto com uma notificação de êxito.</span><span class="sxs-lookup"><span data-stu-id="9178f-116">The redirector on the client receives the packet from the server and passes the data in the packet to the application along with a success notification.</span></span> <span data-ttu-id="9178f-117">Isso é descrito na figura anterior pela seta pontilhada entre o redirecionador do cliente e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9178f-117">This is depicted in the preceding figure by the dotted arrow between the client redirector and the application.</span></span>

<span data-ttu-id="9178f-118">O Windows pode usar uma variedade de protocolos de rede para executar uma operação de e/s de rede, incluindo [o protocolo SMB da Microsoft e a visão geral do protocolo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) e NFS.</span><span class="sxs-lookup"><span data-stu-id="9178f-118">Windows can use a variety of networking protocols to perform a network I/O operation, including [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) and NFS.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9178f-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9178f-119">In this section</span></span>



| <span data-ttu-id="9178f-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="9178f-120">Topic</span></span>                                                                                       | <span data-ttu-id="9178f-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="9178f-121">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="9178f-122">Diferenças em e/s de rede e local</span><span class="sxs-lookup"><span data-stu-id="9178f-122">Differences in Local and Network I/O</span></span>](differences-in-local-and-network-i-o.md)<br/> | <span data-ttu-id="9178f-123">Diferenças entre e/s local e e/s de rede no Windows.</span><span class="sxs-lookup"><span data-stu-id="9178f-123">Differences between local I/O and network I/O on Windows.</span></span><br/> |
| [<span data-ttu-id="9178f-124">Redirecionadores de rede</span><span class="sxs-lookup"><span data-stu-id="9178f-124">Network Redirectors</span></span>](network-redirectors.md)<br/>                                   | <span data-ttu-id="9178f-125">Descreve a funcionalidade de um redirecionador de rede.</span><span class="sxs-lookup"><span data-stu-id="9178f-125">Describes the functionality of a network redirector.</span></span><br/>      |



 

 

 




