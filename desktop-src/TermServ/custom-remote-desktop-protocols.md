---
title: API do provedor de protocolo RDP
description: Você usa a API do provedor de protocolo RDP para criar um protocolo para fornecer comunicação entre o serviço de Serviços de Área de Trabalho Remota e vários clientes.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915861"
---
# <a name="remote-desktop-protocol-provider-api"></a><span data-ttu-id="0367b-103">API do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="0367b-103">Remote Desktop Protocol Provider API</span></span>

<span data-ttu-id="0367b-104">Você usa a API do provedor de protocolo RDP para criar um protocolo para fornecer comunicação entre o serviço de Serviços de Área de Trabalho Remota e vários clientes.</span><span class="sxs-lookup"><span data-stu-id="0367b-104">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

<span data-ttu-id="0367b-105">Quando o Windows Server é carregado, o serviço de Serviços de Área de Trabalho Remota (também conhecido como Gerenciador de conexões remotas (RCM) é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0367b-105">When Windows Server loads, the Remote Desktop Services service (also known as Remote Connection Manager (RCM)) starts.</span></span> <span data-ttu-id="0367b-106">O serviço também inicia objetos de escuta para os provedores de protocolo RDP que, por sua vez, escutam conexões de cliente.</span><span class="sxs-lookup"><span data-stu-id="0367b-106">The service also starts listener objects for the Remote Desktop Protocol Providers that in turn listen for client connections.</span></span> <span data-ttu-id="0367b-107">O serviço e os provedores de protocolo são objetos de modo de usuário que se comunicam usando as APIs discutidas nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="0367b-107">The service and the protocol providers are user-mode objects that communicate by using the APIs discussed in this documentation.</span></span> <span data-ttu-id="0367b-108">Os provedores de protocolo podem se comunicar com drivers de modo kernel usando controles de entrada/saída (IOCTLs).</span><span class="sxs-lookup"><span data-stu-id="0367b-108">The protocol providers can communicate with kernel-mode drivers by using input/output controls (IOCTLs).</span></span> <span data-ttu-id="0367b-109">Isso é mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="0367b-109">This is shown in the following illustration.</span></span>

![arquitetura de API de protocolo personalizado](images/protocol-architecture.png)

<span data-ttu-id="0367b-111">A Microsoft implementou o protocolo RDP (RDP) para fornecer comunicação entre o serviço Serviços de Área de Trabalho Remota e as conexões de cliente.</span><span class="sxs-lookup"><span data-stu-id="0367b-111">Microsoft has implemented the Remote Desktop Protocol (RDP) to provide communication between the Remote Desktop Services service and client connections.</span></span> <span data-ttu-id="0367b-112">Você pode criar seu próprio protocolo usando as interfaces, estruturas, uniões e tipos de enumeração que compõem a API do provedor de protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="0367b-112">You can create your own protocol by using the interfaces, structures, unions, and enumeration types that make up the Remote Desktop Protocol Provider API.</span></span> <span data-ttu-id="0367b-113">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0367b-113">For more information, see the following topics.</span></span>

<dl> <dt>

[<span data-ttu-id="0367b-114">Criando um provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="0367b-114">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dd>

<span data-ttu-id="0367b-115">Informações sobre como criar um provedor de protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="0367b-115">Information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="0367b-116">O Gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço de Serviços de Área de Trabalho Remota é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0367b-116">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

</dd> <dt>

[<span data-ttu-id="0367b-117">Referência do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="0367b-117">Remote Desktop Protocol Provider reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dd>

<span data-ttu-id="0367b-118">Contém interfaces, estruturas, uniões e tipos de enumeração que permitem que você crie um protocolo RDP personalizado (RDP).</span><span class="sxs-lookup"><span data-stu-id="0367b-118">Contains interfaces, structures, unions, and enumeration types that enable you to create a custom Remote Desktop Protocol (RDP).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="0367b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0367b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0367b-120">Sobre Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="0367b-120">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> </dl>

 

 




