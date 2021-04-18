---
title: Criando um provedor de protocolo RDP
description: Informações sobre como criar um provedor de protocolo RDP. O Gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço de Serviços de Área de Trabalho Remota é iniciado.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759948"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a><span data-ttu-id="520a4-104">Criando um provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="520a4-104">Creating a Remote Desktop Protocol Provider</span></span>

<span data-ttu-id="520a4-105">As seções a seguir contêm informações sobre como criar um provedor de protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="520a4-105">The following sections contain information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="520a4-106">O Gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço de Serviços de Área de Trabalho Remota é iniciado.</span><span class="sxs-lookup"><span data-stu-id="520a4-106">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="520a4-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="520a4-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="520a4-108">Registrando o Gerenciador de protocolo</span><span class="sxs-lookup"><span data-stu-id="520a4-108">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
</dt> <dd>

<span data-ttu-id="520a4-109">Você deve criar pelo menos uma entrada de valor de registro para o Gerenciador de protocolo para que o serviço de Serviços de Área de Trabalho Remota possa instanciá-lo.</span><span class="sxs-lookup"><span data-stu-id="520a4-109">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

</dd> <dt>

[<span data-ttu-id="520a4-110">Sequência de chamada de método</span><span class="sxs-lookup"><span data-stu-id="520a4-110">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dd>

<span data-ttu-id="520a4-111">O serviço de Serviços de Área de Trabalho Remota e seu provedor de protocolo chamam uns aos outros em sequências claramente definidas.</span><span class="sxs-lookup"><span data-stu-id="520a4-111">The Remote Desktop Services service and your protocol provider call each other in clearly defined sequences.</span></span>

</dd> </dl>

-   [<span data-ttu-id="520a4-112">Registrando o Gerenciador de protocolo</span><span class="sxs-lookup"><span data-stu-id="520a4-112">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
-   [<span data-ttu-id="520a4-113">Sequência de chamada de método</span><span class="sxs-lookup"><span data-stu-id="520a4-113">Method Call Sequence</span></span>](method-call-sequence.md)

## <a name="related-topics"></a><span data-ttu-id="520a4-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="520a4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="520a4-115">API do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="520a4-115">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dt>

[<span data-ttu-id="520a4-116">Usando Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="520a4-116">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> </dl>

 

 




