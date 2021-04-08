---
title: Windows Remote Management
description: O Gerenciamento Remoto do Windows (Gerenciamento Remoto do Windows) é a implementação da Microsoft do protocolo de WS-Management, um protocolo padrão baseado em SOAP, compatível com firewall, que permite que os sistemas operacionais e de hardware, de fornecedores diferentes, interoperem.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows (WinRM), página inicial
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917335"
---
# <a name="windows-remote-management"></a><span data-ttu-id="dd7bc-105">Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="dd7bc-105">Windows Remote Management</span></span>

## <a name="purpose"></a><span data-ttu-id="dd7bc-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="dd7bc-106">Purpose</span></span>

<span data-ttu-id="dd7bc-107">O WinRM (Gerenciamento Remoto do Windows) é a implementação da Microsoft do [Protocolo WS-Management](ws-management-protocol.md), um protocolo padrão amigável para firewall, baseado no protocolo SOAP, que permite que hardware e sistemas operacionais de fornecedores diferentes interajam.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-107">Windows Remote Management (WinRM) is the Microsoft implementation of [WS-Management Protocol](ws-management-protocol.md), a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span>

<span data-ttu-id="dd7bc-108">A especificação do protocolo WS-Management fornece uma maneira comum de os sistemas acessarem e trocarem informações de gerenciamento em uma infra-estrutura de ti.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-108">The WS-Management protocol specification provides a common way for systems to access and exchange management information across an IT infrastructure.</span></span> <span data-ttu-id="dd7bc-109">O WinRM e a [*IPMI (interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md), juntamente com o [coletor de eventos](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) , são componentes dos recursos de [Gerenciamento de hardware do Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="dd7bc-109">WinRM and [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), along with the [Event Collector](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) are components of the [Windows Hardware Management](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) features.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="dd7bc-110">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="dd7bc-110">Where applicable</span></span>

<span data-ttu-id="dd7bc-111">Você pode usar objetos de script do WinRM, a ferramenta de linha de comando WinRM ou a ferramenta de linha de comando do shell remoto do Windows WinRS para obter dados de gerenciamento de computadores locais e remotos que podem ter [*BMCs (Baseboard Management Controller)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="dd7bc-111">You can use WinRM scripting objects, the WinRM command-line tool, or the Windows Remote Shell command line tool WinRS to obtain management data from local and remote computers that may have [*baseboard management controllers (BMCs)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="dd7bc-112">Se o computador executar uma versão do sistema operacional baseada no Windows que inclui o WinRM, os dados de gerenciamento serão fornecidos pelo [Instrumentação de gerenciamento do Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="dd7bc-112">If the computer runs a Windows-based operating system version that includes WinRM, the management data is supplied by [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

<span data-ttu-id="dd7bc-113">Você também pode obter dados de hardware e do sistema a partir de implementações do protocolo WS-Management que são executadas em sistemas operacionais diferentes do Windows em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-113">You can also obtain hardware and system data from WS-Management protocol implementations running on operating systems other than Windows in your enterprise.</span></span> <span data-ttu-id="dd7bc-114">O WinRM estabelece uma sessão com um computador remoto por meio do protocolo WS-Management baseado em SOAP, em vez de uma conexão por meio do DCOM, como a WMI faz.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-114">WinRM establishes a session with a remote computer through the SOAP-based WS-Management protocol rather than a connection through DCOM, as WMI does.</span></span> <span data-ttu-id="dd7bc-115">Os dados retornados ao protocolo WS-Management são formatados em XML, não em objetos.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-115">Data returned to WS-Management protocol are formatted in XML rather than in objects.</span></span>

<span data-ttu-id="dd7bc-116">O provedor WMI da [IPMI (interface de gerenciamento de plataforma inteligente)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) é um provedor WMI padrão com classes que obtêm dados do sensor do BMC de computadores com hardware apropriado.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-116">The [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI provider is a standard WMI provider with classes that obtain BMC sensor data from computers with appropriate hardware.</span></span> <span data-ttu-id="dd7bc-117">Os dados do IPMI podem ser acessados usando a API de script do WinRM, o [script](/windows/desktop/WmiSdk/scripting-api-for-wmi)do WMI ou APIs [com](/windows/desktop/WmiSdk/com-api-for-wmi) .</span><span class="sxs-lookup"><span data-stu-id="dd7bc-117">IPMI data can be accessed using the WinRM scripting API, the WMI [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi), or [COM](/windows/desktop/WmiSdk/com-api-for-wmi) APIs.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="dd7bc-118">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="dd7bc-118">Developer audience</span></span>

<span data-ttu-id="dd7bc-119">O público-alvo do desenvolvedor é o profissional de ti que escreve scripts para automatizar o gerenciamento de servidores ou o desenvolvedor ISV obtendo dados para aplicativos de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-119">The developer audience is the IT Pro who writes scripts to automate the management of servers or the ISV developer obtaining data for management applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="dd7bc-120">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="dd7bc-120">Run-time requirements</span></span>

<span data-ttu-id="dd7bc-121">O WinRM faz parte do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-121">WinRM is part of the operating system.</span></span> <span data-ttu-id="dd7bc-122">No entanto, para obter dados de computadores remotos, você deve configurar um [*ouvinte*](windows-remote-management-glossary.md#l)do WinRM.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-122">However, to obtain data from remote computers, you must configure a WinRM [*listener*](windows-remote-management-glossary.md#l).</span></span> <span data-ttu-id="dd7bc-123">Para obter mais informações, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="dd7bc-123">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="dd7bc-124">Se um BMC for detectado na inicialização do sistema, o provedor de IPMI será carregado; caso contrário, os objetos de script do WinRM e a ferramenta de linha de comando WinRM ainda estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-124">If a BMC is detected at system startup, then the IPMI provider loads; otherwise, the WinRM scripting objects and the WinRM command-line tool are still available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dd7bc-125">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="dd7bc-125">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="dd7bc-126">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="dd7bc-126">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="dd7bc-127">Link para especificação de protocolo de WS-Management público, arquitetura do WinRM, relação com o WMI, gerenciamento de hardware com o provedor IPMI, configuração e instalação.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-127">Link to public WS-Management protocol specification, WinRM architecture, relationship to WMI, hardware management with the IPMI provider, configuration and installation.</span></span>

</dd> <dt>

[<span data-ttu-id="dd7bc-128">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="dd7bc-128">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="dd7bc-129">Introdução ao uso da API de script do WinRM e do gerenciamento de hardware.</span><span class="sxs-lookup"><span data-stu-id="dd7bc-129">Getting started using the WinRM scripting API and hardware management.</span></span>

</dd> <dt>

[<span data-ttu-id="dd7bc-130">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="dd7bc-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dd>

<span data-ttu-id="dd7bc-131">Lista de interfaces de script definidas pela automação do Microsoft Web Services for Management (WS-Management) e definições de classe das classes WMI criadas pelo provedor IPMI e pelas classes que se comunicam com o driver IPMI para obter os dados do [controlador de gerenciamento de placa-base (BMC)](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="dd7bc-131">List of scripting interfaces defined by Microsoft Web Services for Management (WS-Management) Automation and class definitions of the WMI classes created by the IPMI provider and classes that communicate with the IPMI driver to obtain [baseboard management controller (BMC)](windows-remote-management-glossary.md) data.</span></span>

</dd> </dl>

 

 