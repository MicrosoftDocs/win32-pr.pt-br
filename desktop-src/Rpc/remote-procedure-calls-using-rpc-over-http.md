---
title: Chamadas de procedimentos remotos usando RPC sobre HTTP
description: Os programas de navegador da Internet normalmente empregam o protocolo HTTP como o principal meio de procurar o World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915867"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a><span data-ttu-id="ffdbe-104">Chamadas de procedimentos remotos usando RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="ffdbe-104">Remote Procedure Calls Using RPC over HTTP</span></span>

<span data-ttu-id="ffdbe-105">Os programas de navegador da Internet normalmente empregam o protocolo HTTP como o principal meio de procurar o World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-105">Internet browser programs commonly employ the Hypertext Transport Protocol (HTTP) as the primary means of browsing the World Wide Web.</span></span> <span data-ttu-id="ffdbe-106">O HTTP, portanto, vê uso extensivo na maioria dos computadores atualmente.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-106">HTTP, therefore, sees extensive usage on most computers today.</span></span> <span data-ttu-id="ffdbe-107">A Microsoft ampliou os recursos de seu IIS (servidor de informações da Internet) para fornecer serviços de chamada de procedimento remoto usando HTTP.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-107">Microsoft has extended the capabilities of its Internet Information Server (IIS) to provide remote procedure call services using HTTP.</span></span>

<span data-ttu-id="ffdbe-108">A implementação RPC via http da Microsoft (RPC sobre HTTP) permite que clientes RPC se conectem com segurança e eficiência pela Internet a programas de servidor RPC e executem chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-108">The Microsoft RPC-over-HTTP implementation (RPC over HTTP) allows RPC clients to securely and efficiently connect across the Internet to RPC server programs and execute remote procedure calls.</span></span> <span data-ttu-id="ffdbe-109">Isso é feito com a ajuda de um intermediário conhecido como proxy RPC sobre HTTP ou simplesmente o proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-109">This is accomplished with the help of an intermediary known as the RPC-over-HTTP Proxy, or simply the RPC Proxy.</span></span>

<span data-ttu-id="ffdbe-110">O proxy RPC é executado em um computador IIS.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-110">The RPC Proxy runs on an IIS computer.</span></span> <span data-ttu-id="ffdbe-111">Ele aceita solicitações RPC provenientes da Internet, realiza autenticação, validação e verificações de acesso nessas solicitações e, se a solicitação passar em todos os testes, o proxy RPC encaminha a solicitação para o servidor RPC que executa o processamento real.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-111">It accepts RPC requests coming from the Internet, performs authentication, validation, and access checks on those requests, and if the request passes all tests, RPC Proxy forwards the request to the RPC server that performs the actual processing.</span></span> <span data-ttu-id="ffdbe-112">Com RPC sobre HTTP, o cliente RPC e o servidor não se comunicam diretamente; em vez disso, eles usam o proxy RPC como intermediário.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-112">With RPC over HTTP the RPC client and server do not communicate directly; rather, they use the RPC Proxy as intermediary.</span></span> <span data-ttu-id="ffdbe-113">Esse modelo foi escolhido por muitos motivos.</span><span class="sxs-lookup"><span data-stu-id="ffdbe-113">This model was chosen for many reasons.</span></span> <span data-ttu-id="ffdbe-114">Para obter mais informações, consulte [RPC sobre segurança http](rpc-over-http-security.md).</span><span class="sxs-lookup"><span data-stu-id="ffdbe-114">For more information, see [RPC over HTTP Security](rpc-over-http-security.md).</span></span>

<span data-ttu-id="ffdbe-115">Esta seção fornece uma visão geral do RPC sobre HTTP nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="ffdbe-115">This section provides an overview of RPC over HTTP in the following topics:</span></span>

-   [<span data-ttu-id="ffdbe-116">Usando HTTP como um transporte RPC</span><span class="sxs-lookup"><span data-stu-id="ffdbe-116">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
-   [<span data-ttu-id="ffdbe-117">Segurança de RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="ffdbe-117">RPC over HTTP Security</span></span>](rpc-over-http-security.md)
-   [<span data-ttu-id="ffdbe-118">Requisitos do sistema e interoperabilidade para RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="ffdbe-118">System Requirements and Interoperability for RPC over HTTP</span></span>](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [<span data-ttu-id="ffdbe-119">Configurando computadores para RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="ffdbe-119">Configuring Computers for RPC over HTTP</span></span>](configuring-computers-for-rpc-over-http.md)
-   [<span data-ttu-id="ffdbe-120">Recomendações de implantação de RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="ffdbe-120">RPC over HTTP Deployment Recommendations</span></span>](rpc-over-http-deployment-recommendations.md)

<span data-ttu-id="ffdbe-121">Para obter informações sobre cenários de RPC sobre HTTP em grande volume, consulte [balanceamento de carga do Microsoft RPC](rpc-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="ffdbe-121">For information regarding high volume RPC over HTTP scenarios, please see [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span></span>

 

 




