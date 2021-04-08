---
title: Como os clientes compõem o SPN de um serviço
description: Para autenticar um serviço, um aplicativo cliente compõe um SPN para a instância de serviço à qual ele deve se conectar.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Como os clientes compõem o AD SPN de um serviço
- nome da entidade de serviço AD, como os clientes compõem o SPN de um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915941"
---
# <a name="how-clients-compose-a-services-spn"></a><span data-ttu-id="bf112-105">Como os clientes compõem o SPN de um serviço</span><span class="sxs-lookup"><span data-stu-id="bf112-105">How Clients Compose a Service's SPN</span></span>

<span data-ttu-id="bf112-106">Para autenticar um serviço, um aplicativo cliente compõe um SPN para a instância de serviço à qual ele deve se conectar.</span><span class="sxs-lookup"><span data-stu-id="bf112-106">To authenticate a service, a client application composes an SPN for the service instance to which it must connect.</span></span> <span data-ttu-id="bf112-107">O aplicativo cliente pode usar a função [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para compor um SPN.</span><span class="sxs-lookup"><span data-stu-id="bf112-107">The client application can use the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function to compose an SPN.</span></span> <span data-ttu-id="bf112-108">O cliente especifica os componentes do SPN usando dados conhecidos ou dados recuperados de fontes diferentes do serviço em si.</span><span class="sxs-lookup"><span data-stu-id="bf112-108">The client specifies the components of the SPN using known data or data retrieved from sources other than the service itself.</span></span>

<span data-ttu-id="bf112-109">A forma de um SPN é como mostrado no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="bf112-109">The form of an SPN is as shown in the following form:</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="bf112-110">Neste formulário, " &lt; classe de serviço &gt; " e " &lt; host &gt; " são necessários.</span><span class="sxs-lookup"><span data-stu-id="bf112-110">In this form, "&lt;service class&gt;" and "&lt;host&gt;" are required.</span></span> <span data-ttu-id="bf112-111">" &lt; porta &gt; " e " &lt; nome do serviço &gt; " opcionais.</span><span class="sxs-lookup"><span data-stu-id="bf112-111">"&lt;port&gt;" and "&lt;service name&gt;" optional.</span></span>

<span data-ttu-id="bf112-112">Normalmente, o cliente reconhece a parte de " &lt; classe &gt; de serviço" do nome e reconhece qual dos componentes opcionais incluir no SPN.</span><span class="sxs-lookup"><span data-stu-id="bf112-112">Typically, the client recognizes the "&lt;service class&gt;" part of the name, and recognizes which of the optional components to include in the SPN.</span></span> <span data-ttu-id="bf112-113">O cliente pode recuperar componentes do SPN de fontes como um SCP (ponto de conexão de serviço) ou entrada de usuário.</span><span class="sxs-lookup"><span data-stu-id="bf112-113">The client can retrieve components of the SPN from sources such as a service connection point (SCP) or user input.</span></span> <span data-ttu-id="bf112-114">Por exemplo, o cliente pode ler o atributo **serviceDNSName** do SCP de um serviço para obter o &lt; componente "host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="bf112-114">For example, the client can read the **serviceDNSName** attribute of a service's SCP to get the "&lt;host&gt;" component.</span></span> <span data-ttu-id="bf112-115">O atributo **serviceDNSName** contém o nome DNS do servidor no qual a instância de serviço está em execução ou o nome DNS dos registros SRV que contêm os dados do host para réplicas de serviço.</span><span class="sxs-lookup"><span data-stu-id="bf112-115">The **serviceDNSName** attribute contains either the DNS name of the server on which the service instance is running or the DNS name of SRV records containing the host data for service replicas.</span></span> <span data-ttu-id="bf112-116">O &lt; componente "nome do serviço &gt; ", usado somente para serviços replicáveis, pode ser o nome distinto do SCP do serviço, o nome DNS do domínio servido pelo serviço ou o nome DNS dos registros SRV ou MX.</span><span class="sxs-lookup"><span data-stu-id="bf112-116">The "&lt;service name&gt;" component, used only for replicable services, can be the distinguished name of the service's SCP, the DNS name of the domain served by the service, or the DNS name of SRV or MX records.</span></span>

<span data-ttu-id="bf112-117">Para obter mais informações e um exemplo de código usado para compor um SPN para um serviço, consulte [como um cliente autentica um serviço de soquetes do Windows baseado em SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span><span class="sxs-lookup"><span data-stu-id="bf112-117">For more information and a code example used to compose an SPN for a service, see [How a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span></span>

<span data-ttu-id="bf112-118">Para obter mais informações e uma descrição dos componentes do SPN, consulte [formatos de nome para SPNs exclusivos](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="bf112-118">For more information and a description of the SPN components, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

 

 




