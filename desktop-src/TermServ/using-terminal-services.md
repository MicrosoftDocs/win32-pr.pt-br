---
title: Usando Serviços de Área de Trabalho Remota
description: Como programar no ambiente de Serviços de Área de Trabalho Remota e como estender a tecnologia Serviços de Área de Trabalho Remota (anteriormente conhecida como serviços de terminal) para a Web usando Conexão Web de Área de Trabalho Remota.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761796"
---
# <a name="using-remote-desktop-services"></a><span data-ttu-id="232fd-104">Usando Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="232fd-104">Using Remote Desktop Services</span></span>

<span data-ttu-id="232fd-105">As seções a seguir descrevem como programar no ambiente de Serviços de Área de Trabalho Remota e como estender a tecnologia Serviços de Área de Trabalho Remota (anteriormente conhecida como serviços de terminal) para a Web usando Conexão Web de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="232fd-105">The following sections describe how to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span> <span data-ttu-id="232fd-106">Se você estiver procurando informações do usuário para Área de Trabalho Remota conexões, consulte [conectar-se a outro computador usando conexão de área de trabalho remota](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span><span class="sxs-lookup"><span data-stu-id="232fd-106">If you are looking for user information for Remote Desktop connections, See [Connect to another computer using Remote Desktop Connection](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span></span>

> [!Note]  
> <span data-ttu-id="232fd-107">Este tópico destina-se a desenvolvedores de software.</span><span class="sxs-lookup"><span data-stu-id="232fd-107">This topic is for software developers.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="232fd-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="232fd-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="232fd-109">Detectando se a função de Serviços de Área de Trabalho Remota está instalada</span><span class="sxs-lookup"><span data-stu-id="232fd-109">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

<span data-ttu-id="232fd-110">Exemplo de código C# que mostra um método que retorna **true** se a função de servidor serviços de área de trabalho remota estiver instalada e em execução ou **false** caso contrário, começando com o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="232fd-110">C# code example that shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise, beginning with Windows Server 2008.</span></span>

</dd> <dt>

[<span data-ttu-id="232fd-111">Extensão do agente de sessão dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="232fd-111">Extending Terminal Services Session Broker</span></span>](extending-ts-session-broker.md)
</dt> <dd>

<span data-ttu-id="232fd-112">Você pode estender o agente de Sessão TS usando a interface com do [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="232fd-112">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span>

</dd> <dt>

[<span data-ttu-id="232fd-113">Implementando um enumerador de ponto de extremidade de áudio personalizado</span><span class="sxs-lookup"><span data-stu-id="232fd-113">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

<span data-ttu-id="232fd-114">A partir do Windows Server 2008 R2, você pode implementar um enumerador personalizado de ponto de extremidade de áudio remoto como parte de um provedor de protocolo Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="232fd-114">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="232fd-115">Monikers de sessão</span><span class="sxs-lookup"><span data-stu-id="232fd-115">Session Monikers</span></span>](session-monikers.md)
</dt> <dd>

<span data-ttu-id="232fd-116">O COM distribuído (DCOM) permite a ativação de objeto por sessão usando um moniker de sessão fornecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="232fd-116">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied session moniker.</span></span>

</dd> <dt>

[<span data-ttu-id="232fd-117">Usando a extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário</span><span class="sxs-lookup"><span data-stu-id="232fd-117">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

<span data-ttu-id="232fd-118">A administração de propriedades de usuário específicas de Serviços de Área de Trabalho Remota é possível usando os métodos implementados pela extensão ADSI (Active Directory Service Interfaces), que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="232fd-118">Administration of Remote Desktop Services-specific user properties is possible by using the methods implemented by the Active Directory Service Interfaces (ADSI) extension, which is packaged with the dynamic-link library Tsuserex.dll.</span></span>

</dd> <dt>

[<span data-ttu-id="232fd-119">Usando a API de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="232fd-119">Using the Remote Desktop Services API</span></span>](using-the-terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="232fd-120">Descreve como você pode usar a API Serviços de Área de Trabalho Remota para permitir que os aplicativos executem tarefas em um ambiente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="232fd-120">Describes how you can use the Remote Desktop Services API to enable applications to perform tasks in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="232fd-121">Usando a API de virtualização Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="232fd-121">Using the Remote Desktop Virtualization API</span></span>](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

<span data-ttu-id="232fd-122">Os desenvolvedores podem usar essa API para personalizar a lógica que o Conexão de Área de Trabalho Remota Broker (agente de conexão de área de trabalho remota) usa para determinar o melhor destino para uma conexão de cliente de entrada.</span><span class="sxs-lookup"><span data-stu-id="232fd-122">Developers can use this API to customize the logic that Remote Desktop Connection Broker (RD Connection Broker) uses to determine the best destination for an incoming client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="232fd-123">Interface WSDL para soluções de VDI personalizadas</span><span class="sxs-lookup"><span data-stu-id="232fd-123">WSDL Interface for Custom VDI Solutions</span></span>](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

<span data-ttu-id="232fd-124">Os desenvolvedores podem criar serviços Web personalizados que gerenciam soluções de VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="232fd-124">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

</dd> </dl>

<span data-ttu-id="232fd-125">Para obter mais informações, consulte [diretrizes de programação de serviços de área de trabalho remota](terminal-services-programming-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="232fd-125">For more information, see [Remote Desktop Services Programming Guidelines](terminal-services-programming-guidelines.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="232fd-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="232fd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="232fd-127">Os serviços de terminal agora estão Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="232fd-127">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="232fd-128">Detectando o ambiente de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="232fd-128">Detecting the Remote Desktop Services Environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




