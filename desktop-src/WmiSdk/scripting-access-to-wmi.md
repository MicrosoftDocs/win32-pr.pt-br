---
description: Os scripts podem acessar todas as classes WMI para objetos de hardware e software.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Script de acesso ao WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165212"
---
# <a name="scripting-access-to-wmi"></a><span data-ttu-id="f7108-103">Script de acesso ao WMI</span><span class="sxs-lookup"><span data-stu-id="f7108-103">Scripting Access to WMI</span></span>

<span data-ttu-id="f7108-104">Os scripts podem acessar todas as classes WMI para objetos de hardware e software.</span><span class="sxs-lookup"><span data-stu-id="f7108-104">Scripts can access all WMI classes for hardware and software objects.</span></span> <span data-ttu-id="f7108-105">Os scripts do WSH (Windows Script Host) podem executar operações em objetos do sistema de arquivos, manipular impressoras de rede ou alterar variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="f7108-105">Windows Script Host (WSH) scripts can perform operations on file system objects, manipulate network printers, or change environment variables.</span></span> <span data-ttu-id="f7108-106">Você pode encontrar uma variedade de tarefas de administrador e uma breve orientação sobre como realizá-las no WMI em [tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="f7108-106">You can find a variety of administrator tasks and brief guidance on how to accomplish them in WMI at [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="f7108-107">Para obter mais informações e exemplos, consulte o [repositório de scripts](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)do TechNet ScriptCenter.</span><span class="sxs-lookup"><span data-stu-id="f7108-107">For more information and examples, see the TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span></span>

<span data-ttu-id="f7108-108">Se você for novo no script ou em scripts específicos do WMI, consulte a seção do TechNet ScriptCenter [introdução](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span><span class="sxs-lookup"><span data-stu-id="f7108-108">If you are new to scripting or to WMI-specific scripting, see the TechNet ScriptCenter section [Getting Started](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span></span>

<span data-ttu-id="f7108-109">Com a [API de script para WMI](scripting-api-for-wmi.md), você pode desenvolver scripts rápidos e simples ou aplicativos complexos.</span><span class="sxs-lookup"><span data-stu-id="f7108-109">With the [Scripting API for WMI](scripting-api-for-wmi.md), you can develop quick, simple scripts or complex applications.</span></span> <span data-ttu-id="f7108-110">O script oferece o mesmo recurso de obter informações ou configurar a maioria dos objetos em uma empresa como você teria por meio de um aplicativo C++ ou C#.</span><span class="sxs-lookup"><span data-stu-id="f7108-110">Scripting gives you the same capability of getting information or of configuring most objects in an enterprise as you would have through a C++ or C# application.</span></span> <span data-ttu-id="f7108-111">Para obter mais informações, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7108-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f7108-112">Não é possível gravar um [*provedor WMI*](gloss-p.md) no script.</span><span class="sxs-lookup"><span data-stu-id="f7108-112">You cannot write a [*WMI provider*](gloss-p.md) in script.</span></span> <span data-ttu-id="f7108-113">Para obter mais informações, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f7108-113">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="f7108-114">Os scripts do WMI podem ser escritos em qualquer linguagem de script que possa interagir com objetos ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f7108-114">WMI scripts can be written in any scripting language that can interact with ActiveX objects.</span></span>

<span data-ttu-id="f7108-115">O Windows PowerShell fornece um ambiente simples para a administração e script do WMI.</span><span class="sxs-lookup"><span data-stu-id="f7108-115">Windows PowerShell provides a simple environment for WMI administration and scripting.</span></span> <span data-ttu-id="f7108-116">Para obter mais informações sobre o PowerShell, consulte [introdução com o Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="f7108-116">For more information about PowerShell, see [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span>

<span data-ttu-id="f7108-117">Os scripts de ADSI (Active Directory Service Interfaces) fornecem acesso a objetos Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f7108-117">Active Directory Service Interfaces (ADSI) scripts provides access to Active Directory Domain Services (AD DS) objects.</span></span> <span data-ttu-id="f7108-118">Os scripts do WSH e do ADSI acessam objetos e permitem que os procedimentos não estejam disponíveis por meio de arquivos em lotes.</span><span class="sxs-lookup"><span data-stu-id="f7108-118">Both WSH and ADSI scripts access objects and allow procedures not available through batch files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7108-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7108-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7108-120">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="f7108-120">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="f7108-121">API de script para WMI</span><span class="sxs-lookup"><span data-stu-id="f7108-121">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
