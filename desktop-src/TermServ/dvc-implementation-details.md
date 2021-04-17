---
title: Detalhes da implementação do DVC
description: Esta seção contém informações sobre como gravar um módulo de cliente de canal virtual dinâmico (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769388"
---
# <a name="dvc-implementation-details"></a><span data-ttu-id="de1c3-103">Detalhes da implementação do DVC</span><span class="sxs-lookup"><span data-stu-id="de1c3-103">DVC Implementation Details</span></span>

<span data-ttu-id="de1c3-104">Esta seção contém informações sobre como gravar um módulo de cliente de canal virtual dinâmico (DVC).</span><span class="sxs-lookup"><span data-stu-id="de1c3-104">This section contains information about how to write a dynamic virtual channel (DVC) client module.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="de1c3-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="de1c3-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="de1c3-106">Escrevendo um módulo de DVC de cliente</span><span class="sxs-lookup"><span data-stu-id="de1c3-106">Writing a Client DVC Module</span></span>](writing-a-client-dvc-component.md)
</dt> <dd>

<span data-ttu-id="de1c3-107">Para gravar um módulo de cliente de canal virtual dinâmico (DVC), você deve primeiro implementar e registrar um plug-in de cliente Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="de1c3-107">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="de1c3-108">Registro de plug-in do DVC</span><span class="sxs-lookup"><span data-stu-id="de1c3-108">DVC plug-in registration</span></span>](dvc-plug-in-registration.md)
</dt> <dd>

<span data-ttu-id="de1c3-109">Descreve a sintaxe para a entrada de plug-in de canal virtual dinâmico (DVC) para o cliente de Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="de1c3-109">Describes syntax for the dynamic virtual channel (DVC) plug-in entry for the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="de1c3-110">Iniciando um ouvinte DVC</span><span class="sxs-lookup"><span data-stu-id="de1c3-110">Starting a DVC Listener</span></span>](starting-a-dvc-listener.md)
</dt> <dd>

<span data-ttu-id="de1c3-111">Para estabelecer uma conexão bem-sucedida entre dois módulos DVC (canal virtual dinâmico) em execução no cliente e servidor do Conexão de Área de Trabalho Remota (RDC), um ouvinte DVC deve estar em execução e em um estado de escuta.</span><span class="sxs-lookup"><span data-stu-id="de1c3-111">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

</dd> <dt>

[<span data-ttu-id="de1c3-112">Aceitando uma conexão</span><span class="sxs-lookup"><span data-stu-id="de1c3-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> <dd>

<span data-ttu-id="de1c3-113">Em algum momento, o cliente do DVC (canal virtual dinâmico) solicitará uma conexão com o ouvinte DVC.</span><span class="sxs-lookup"><span data-stu-id="de1c3-113">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span>

</dd> <dt>

[<span data-ttu-id="de1c3-114">Gravando dados usando um canal DVC</span><span class="sxs-lookup"><span data-stu-id="de1c3-114">Writing Data by Using a DVC Channel</span></span>](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

<span data-ttu-id="de1c3-115">Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente.</span><span class="sxs-lookup"><span data-stu-id="de1c3-115">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span>

</dd> <dt>

[<span data-ttu-id="de1c3-116">Testando e Depurando</span><span class="sxs-lookup"><span data-stu-id="de1c3-116">Testing and Debugging</span></span>](testing-and-debugging.md)
</dt> <dd>

<span data-ttu-id="de1c3-117">Há um ouvinte de "eco" que é implementado pelo cliente de Conexão de Área de Trabalho Remota (RDC), que está sempre presente e escutando conexões de entrada.</span><span class="sxs-lookup"><span data-stu-id="de1c3-117">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span>

</dd> <dt>

[<span data-ttu-id="de1c3-118">Exemplo de plug-in de cliente DVC</span><span class="sxs-lookup"><span data-stu-id="de1c3-118">DVC Client Plug-in Example</span></span>](dvc-client-plug-in-example.md)
</dt> <dd>

<span data-ttu-id="de1c3-119">Exemplo de código C++ que mostra como criar um plug-in de Conexão de Área de Trabalho Remota (RDC) cliente Dynamic virtual Channel (DVC).</span><span class="sxs-lookup"><span data-stu-id="de1c3-119">C++ code sample that shows how to create a Remote Desktop Connection (RDC) client dynamic virtual channel (DVC) plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="de1c3-120">Exemplo de módulo de servidor DVC</span><span class="sxs-lookup"><span data-stu-id="de1c3-120">DVC Server Module Example</span></span>](dvc-server-component-example.md)
</dt> <dd>

<span data-ttu-id="de1c3-121">Exemplo de código C++ que mostra como criar o módulo DVC (canal virtual dinâmico) do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="de1c3-121">C++ code sample that shows how to create the server-side dynamic virtual channel (DVC) module.</span></span>

</dd> </dl>

 

 




