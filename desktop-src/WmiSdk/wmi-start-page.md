---
description: Instrumentação de Gerenciamento do Windows (WMI) é a infraestrutura para dados de gerenciamento e operações em sistemas operacionais baseados no Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Instrumentação de Gerenciamento do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770564"
---
# <a name="windows-management-instrumentation"></a><span data-ttu-id="b20fd-103">Instrumentação de Gerenciamento do Windows</span><span class="sxs-lookup"><span data-stu-id="b20fd-103">Windows Management Instrumentation</span></span>

## <a name="purpose"></a><span data-ttu-id="b20fd-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="b20fd-104">Purpose</span></span>

<span data-ttu-id="b20fd-105">Instrumentação de Gerenciamento do Windows (WMI) é a infraestrutura para dados de gerenciamento e operações em sistemas operacionais baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="b20fd-105">Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.</span></span> <span data-ttu-id="b20fd-106">Você pode gravar scripts ou aplicativos WMI para automatizar tarefas administrativas em computadores remotos, mas o WMI também fornece dados de gerenciamento para outras partes do sistema operacional e produtos, por exemplo System Center Operations Manager, anteriormente Microsoft Operations Manager (MOM) ou Gerenciamento Remoto do Windows ([WinRM](/windows/desktop/WinRM/portal)).</span><span class="sxs-lookup"><span data-stu-id="b20fd-106">You can write WMI scripts or applications to automate administrative tasks on remote computers but WMI also supplies management data to other parts of the operating system and products, for example System Center Operations Manager, formerly Microsoft Operations Manager (MOM), or Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span></span>

> [!Note]  
> <span data-ttu-id="b20fd-107">A documentação a seguir destina-se a desenvolvedores e administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="b20fd-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="b20fd-108">Se você for um usuário final que recebeu uma mensagem de erro relacionada ao WMI, vá para [suporte da Microsoft](https://support.microsoft.com/) e procure o código de erro que você vê na mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="b20fd-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="b20fd-109">Para obter mais informações sobre como solucionar problemas com scripts WMI e o serviço WMI, consulte o [WMI não está funcionando!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b20fd-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span></span>

 

> [!Note]  
> <span data-ttu-id="b20fd-110">O WMI tem suporte total da Microsoft; no entanto, a versão mais recente do controle e script administrativo está disponível por meio da MI (infraestrutura de gerenciamento do Windows).</span><span class="sxs-lookup"><span data-stu-id="b20fd-110">WMI is fully supported by Microsoft; however, the latest version of administrative scripting and control is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="b20fd-111">MI é totalmente compatível com as versões anteriores do WMI e fornece um host de recursos e benefícios que facilitam ainda mais o projeto e o desenvolvimento de provedores e clientes.</span><span class="sxs-lookup"><span data-stu-id="b20fd-111">MI is fully compatible with previous versions of WMI, and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span> <span data-ttu-id="b20fd-112">Para obter mais informações, consulte [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span><span class="sxs-lookup"><span data-stu-id="b20fd-112">For more information, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="b20fd-113">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="b20fd-113">Where applicable</span></span>

<span data-ttu-id="b20fd-114">O WMI pode ser usado em todos os aplicativos baseados no Windows e é mais útil em aplicativos empresariais e scripts administrativos.</span><span class="sxs-lookup"><span data-stu-id="b20fd-114">WMI can be used in all Windows-based applications, and is most useful in enterprise applications and administrative scripts.</span></span>

<span data-ttu-id="b20fd-115">Os administradores do sistema podem encontrar informações sobre como usar o WMI no TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)e em vários livros sobre o WMI.</span><span class="sxs-lookup"><span data-stu-id="b20fd-115">System administrators can find information about using WMI at the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx), and in various books about WMI.</span></span> <span data-ttu-id="b20fd-116">Para obter mais informações, consulte [mais informações](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="b20fd-116">For more information, see [Further Information](further-information.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b20fd-117">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="b20fd-117">Developer audience</span></span>

<span data-ttu-id="b20fd-118">O WMI foi projetado para programadores que usam o C/C++, o aplicativo Microsoft Visual Basic ou uma linguagem de script que tem um mecanismo no Windows e manipula objetos ActiveX da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b20fd-118">WMI is designed for programmers who use C/C++, the Microsoft Visual Basic application, or a scripting language that has an engine on Windows and handles Microsoft ActiveX objects.</span></span> <span data-ttu-id="b20fd-119">Embora alguma familiaridade com a programação COM seja útil, os desenvolvedores de C++ que estão escrevendo aplicativos podem encontrar bons exemplos de introdução à [criação de um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="b20fd-119">While some familiarity with COM programming is helpful, C++ developers who are writing applications can find good examples for getting started at [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

<span data-ttu-id="b20fd-120">Para desenvolver provedores de código gerenciado ou aplicativos em C# ou Visual Basic .NET usando o .NET Framework, consulte [WMI no .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="b20fd-120">To develop managed code providers or applications in C# or Visual Basic .NET using the .NET Framework, see [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

<span data-ttu-id="b20fd-121">Muitos administradores e profissionais de ti acessam o WMI por meio do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b20fd-121">Many administrators and IT professionals access WMI through PowerShell.</span></span> <span data-ttu-id="b20fd-122">O cmdlet Get-WMI para o PowerShell permite que você recupere informações para um repositório WMI local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="b20fd-122">The Get-WMI cmdlet for PowerShell enables you to retrieve information for a local or remote WMI repository.</span></span> <span data-ttu-id="b20fd-123">Assim, vários tópicos e classes, especialmente na seção [criando clientes WMI](creating-wmi-clients.md) , contêm exemplos do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b20fd-123">As such, a number of topics and classes, especially in the [Creating WMI Clients](creating-wmi-clients.md) section, contain PowerShell examples.</span></span> <span data-ttu-id="b20fd-124">Para obter informações adicionais sobre como usar o PowerShell, consulte [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) e [scripts com o Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="b20fd-124">For additional information on using PowerShell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) and [Scripting with Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b20fd-125">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="b20fd-125">Run-time requirements</span></span>

<span data-ttu-id="b20fd-126">Para obter mais informações sobre qual sistema operacional é necessário para usar um elemento de API específico ou uma classe WMI, consulte a seção requisitos de cada tópico na documentação do WMI.</span><span class="sxs-lookup"><span data-stu-id="b20fd-126">For more information about which operating system is required to use a specific API element or WMI class, see the Requirements section of each topic in the WMI documentation.</span></span>

<span data-ttu-id="b20fd-127">Se um componente esperado parece estar ausente, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="b20fd-127">If an expected component appears to be missing, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

<span data-ttu-id="b20fd-128">Você não precisa baixar ou instalar um SDK (desenvolvimento de software) específico para criar scripts ou aplicativos para o WMI.</span><span class="sxs-lookup"><span data-stu-id="b20fd-128">You do not need to download or install a specific software development (SDK) in order to create scripts or applications for WMI.</span></span> <span data-ttu-id="b20fd-129">No entanto, há algumas ferramentas administrativas do WMI que os desenvolvedores consideram úteis.</span><span class="sxs-lookup"><span data-stu-id="b20fd-129">However, there are some WMI administrative tools that developers find useful.</span></span> <span data-ttu-id="b20fd-130">Para obter mais informações, consulte a seção downloads em [mais informações](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="b20fd-130">For more information, see the Downloads section in [Further Information](further-information.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b20fd-131">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b20fd-131">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b20fd-132">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="b20fd-132">About WMI</span></span>](about-wmi.md)
</dt> <dd>

<span data-ttu-id="b20fd-133">Informações gerais sobre o WMI.</span><span class="sxs-lookup"><span data-stu-id="b20fd-133">General information about WMI.</span></span>

</dd> <dt>

[<span data-ttu-id="b20fd-134">Usando o WMI</span><span class="sxs-lookup"><span data-stu-id="b20fd-134">Using WMI</span></span>](using-wmi.md)
</dt> <dd>

<span data-ttu-id="b20fd-135">Informações sobre como desenvolver aplicativos para usar o WMI, que inclui informações sobre ferramentas.</span><span class="sxs-lookup"><span data-stu-id="b20fd-135">Information about how to develop applications to use WMI, which includes information about tools.</span></span>

</dd> <dt>

[<span data-ttu-id="b20fd-136">Referência de WMI</span><span class="sxs-lookup"><span data-stu-id="b20fd-136">WMI Reference</span></span>](wmi-reference.md)
</dt> <dd>

<span data-ttu-id="b20fd-137">Documentação sobre as classes WMI, as classes WMI C++, a API COM do WMI, a API de script e outros materiais de referência do WMI.</span><span class="sxs-lookup"><span data-stu-id="b20fd-137">Documentation about the WMI classes, WMI C++ classes, WMI COM API, Scripting API, and other WMI reference material.</span></span>

</dd> </dl>

 

 
