---
title: Extensão do agente de sessão dos serviços de terminal
description: Você pode estender TS \ 160; Agente de sessão usando a interface COM do IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641597"
---
# <a name="extending-terminal-services-session-broker"></a><span data-ttu-id="e3fd3-103">Extensão do agente de sessão dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="e3fd3-103">Extending Terminal Services Session Broker</span></span>

<span data-ttu-id="e3fd3-104">O agente de sessão dos serviços de terminal (agente de Sessão TS) determina se um usuário que inicia uma conexão já tem uma sessão aberta.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-104">Terminal Services Session Broker (TS Session Broker) determines whether a user who initiates a connection has a session open already.</span></span> <span data-ttu-id="e3fd3-105">Nesse caso, o agente de Sessão TS roteia a conexão de entrada para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) com a sessão existente.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-105">If so, TS Session Broker routes the incoming connection to the Remote Desktop Session Host (RD Session Host) server with the existing session.</span></span> <span data-ttu-id="e3fd3-106">Caso contrário, o agente de Sessão TS roteia a conexão de entrada para o servidor de Host da Sessão RD com o menor número de sessões.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-106">If not, TS Session Broker routes the incoming connection to the RD Session Host server with the fewest sessions.</span></span>

<span data-ttu-id="e3fd3-107">Você pode estender o agente de Sessão TS usando a interface com do [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="e3fd3-107">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span> <span data-ttu-id="e3fd3-108">Você pode usar essa interface para gerenciar conexões com servidores Host da Sessão RD, bem como qualquer tipo de conexão de protocolo RDP (RDP), por exemplo, conexões com máquinas virtuais convidadas que estejam executando o VECD (Desktop central do Windows Vista Enterprise) em um host de máquina virtual do Windows Server 2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-108">You can use this interface to manage connections to RD Session Host servers as well as any kind of Remote Desktop Protocol (RDP) connection, for example, connections to guest virtual machines that are running Windows Vista Enterprise Centralized Desktop (VECD) on a Windows Server 2008 Hyper-V virtual machine host.</span></span>

<span data-ttu-id="e3fd3-109">A interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) oferece vários benefícios:</span><span class="sxs-lookup"><span data-stu-id="e3fd3-109">The [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) interface offers several benefits:</span></span>

-   <span data-ttu-id="e3fd3-110">Não é necessário instalar um agente no cliente ou no servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-110">It is not necessary to install an agent on the client or the RD Session Host server.</span></span>
-   <span data-ttu-id="e3fd3-111">O plug-in pode interagir diretamente com outros serviços de Serviços de Área de Trabalho Remota função, como o gateway de Área de Trabalho Remota (gateway de área de trabalho remota) e contar com informações do agente de Sessão TS sobre Estados de sessão e de computador.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-111">The plug-in can interact seamlessly with other Remote Desktop Services role services, such as Remote Desktop Gateway (RD Gateway), and rely on information from TS Session Broker about session and computer states.</span></span>
-   <span data-ttu-id="e3fd3-112">Você pode usar o plug-in para gerenciar conexões com dispositivos cliente ou de servidor que dão suporte a RDP 5,2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-112">You can use the plug-in to manage connections with client or server devices that support RDP 5.2 or later.</span></span>
-   <span data-ttu-id="e3fd3-113">Você pode usar o plug-in para habilitar as soluções de área de trabalho do Windows Vista Enterprise central.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-113">You can use the plug-in to enable Windows Vista Enterprise Centralized Desktop solutions.</span></span>

<span data-ttu-id="e3fd3-114">Ao implementar os métodos dessa interface, tenha em mente os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="e3fd3-114">When you implement the methods of this interface, keep the following points in mind:</span></span>

-   <span data-ttu-id="e3fd3-115">O agente de Sessão TS pode chamar os métodos desse objeto COM de vários threads.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-115">TS Session Broker might call the methods of this COM object from multiple threads.</span></span>
-   <span data-ttu-id="e3fd3-116">Se qualquer um dos métodos chamados não retornar imediatamente e com êxito, o agente de Sessão TS não fará mais chamadas para o plug-in e será revertido para sua lógica de balanceamento de carga nativa.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-116">If any of the called methods do not return immediately and successfully, TS Session Broker makes no more calls to the plug-in and reverts to its native load-balancing logic.</span></span> <span data-ttu-id="e3fd3-117">Para retomar as chamadas para o plug-in, você deve reiniciar o serviço de agente de sessão dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-117">To resume calls to the plug-in, you must restart the Terminal Services Session Broker service.</span></span>
-   <span data-ttu-id="e3fd3-118">Você deve registrar o plug-in como um objeto COM em todo o sistema usando Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-118">You must register the plug-in as a system-wide COM object by using Regsvr32.exe.</span></span> <span data-ttu-id="e3fd3-119">Como o serviço de agente de sessão dos serviços de terminal é executado na conta "NetworkService", você deve conceder à conta "NetworkService" as permissões de inicialização, ativação e acesso necessárias usando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-119">Because the Terminal Services Session Broker service runs under the "NetworkService" account, you must give the "NetworkService" account the required launch, activation, and access permissions by using Dcomcnfg.exe.</span></span> <span data-ttu-id="e3fd3-120">O serviço de agente de sessão dos serviços de terminal procura o CLSID do objeto COM que representa o plug-in na seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="e3fd3-120">The Terminal Services Session Broker service looks for the CLSID of the COM object that represents the plug-in in the following registry subkey:</span></span>

    <span data-ttu-id="e3fd3-121">**HKEY \_ \_Computador local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **Parameters** \\ **ExtensibilityPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-121">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**Tssdis**\\**Parameters**\\**ExtensibilityPluginCLSID**</span></span>

<span data-ttu-id="e3fd3-122">Para obter mais informações sobre Dcomcnfg.exe, consulte [habilitando a segurança com usando DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span><span class="sxs-lookup"><span data-stu-id="e3fd3-122">For more information about Dcomcnfg.exe, see [Enabling COM Security Using DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3fd3-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3fd3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3fd3-124">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-124">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 