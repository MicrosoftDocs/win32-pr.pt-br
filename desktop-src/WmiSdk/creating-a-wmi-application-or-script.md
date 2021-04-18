---
description: Qualquer linguagem de script, como o VBScript, que funciona com objetos ActiveX pode acessar dados do WMI. Os aplicativos podem acessar o WMI em C++, usando a API COM para WMI ou no Visual Basic, usando a biblioteca de tipos Wbemdisp. tlb e a API de script para WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Criando um script ou aplicativo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810778"
---
# <a name="creating-a-wmi-application-or-script"></a><span data-ttu-id="4b280-105">Criando um script ou aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="4b280-105">Creating a WMI Application or Script</span></span>

<span data-ttu-id="4b280-106">Qualquer linguagem de script, como o VBScript, que funciona com objetos ActiveX pode acessar dados do WMI.</span><span class="sxs-lookup"><span data-stu-id="4b280-106">Any scripting language, such as VBScript, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="4b280-107">Os aplicativos podem acessar o WMI em C++, usando a [API com para WMI](com-api-for-wmi.md) ou no Visual Basic, usando a [biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb e a [API de script para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4b280-107">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb [type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="4b280-108">.</span><span class="sxs-lookup"><span data-stu-id="4b280-108">.</span></span> <span data-ttu-id="4b280-109">Você pode obter dados por meio do WMI escrevendo um script, uma página de Active Server (ASP) ou um aplicativo HTML (HTA).</span><span class="sxs-lookup"><span data-stu-id="4b280-109">You can obtain data through WMI by writing a script, an Active Server Page (ASP), or an HTML application (HTA).</span></span> <span data-ttu-id="4b280-110">Você também pode usar o Windows PowerShell para obter dados ou gravar scripts.</span><span class="sxs-lookup"><span data-stu-id="4b280-110">You can also use Windows PowerShell to obtain data or write scripts.</span></span> <span data-ttu-id="4b280-111">Para obter mais informações, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) e [introdução com o Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="4b280-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span> <span data-ttu-id="4b280-112">O TechNet ScriptCenter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contém centenas de exemplos de script.</span><span class="sxs-lookup"><span data-stu-id="4b280-112">The TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contains hundreds of scripting examples.</span></span> <span data-ttu-id="4b280-113">Para obter mais informações sobre recursos de impressão e online, consulte [mais informações](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="4b280-113">For more information about print and online resources, see [Further Information](further-information.md).</span></span>

<span data-ttu-id="4b280-114">O procedimento a seguir descreve como se conectar ao serviço WMI e ao armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="4b280-114">The following procedure describes how to connect to the WMI service and data store.</span></span>

<span data-ttu-id="4b280-115">**Para se conectar ao serviço WMI e ao armazenamento de dados**</span><span class="sxs-lookup"><span data-stu-id="4b280-115">**To connect to the WMI service and data store**</span></span>

1.  <span data-ttu-id="4b280-116">Localize o serviço WMI em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="4b280-116">Locate the WMI service on a specific machine.</span></span>
2.  <span data-ttu-id="4b280-117">Conecte-se a um ou mais namespaces do WMI.</span><span class="sxs-lookup"><span data-stu-id="4b280-117">Connect to one or more WMI namespaces.</span></span>

<span data-ttu-id="4b280-118">Essas operações são diferentes em C++, Visual Basic, .NET Framework linguagens ou ao usar um script.</span><span class="sxs-lookup"><span data-stu-id="4b280-118">These operations are different in C++, Visual Basic, .NET Framework languages, or when using a script.</span></span> <span data-ttu-id="4b280-119">Scripts e Visual Basic aplicativos devem acessar classes cujas instâncias são fornecidas com os dados por provedores existentes.</span><span class="sxs-lookup"><span data-stu-id="4b280-119">Scripts and Visual Basic applications must access classes whose instances are supplied with data by existing providers.</span></span> <span data-ttu-id="4b280-120">Mas os aplicativos escritos em C++ podem fazer mais.</span><span class="sxs-lookup"><span data-stu-id="4b280-120">But applications written in C++ can do more.</span></span> <span data-ttu-id="4b280-121">Por exemplo, um aplicativo escrito em C++ pode enviar eventos, mas um script WMI só pode assinar eventos de recebimento.</span><span class="sxs-lookup"><span data-stu-id="4b280-121">For example, an application written in C++ can send events, but a WMI script can only subscribe to receive events.</span></span>

<span data-ttu-id="4b280-122">Um provedor WMI só pode ser escrito em C++ ou usando o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4b280-122">A WMI provider can be written only in C++ or using the .NET Framework.</span></span> <span data-ttu-id="4b280-123">Para obter mais informações sobre como escrever aplicativos em C# ou Visual Basic .NET, consulte [visão geral do WMI .net](/previous-versions/bb404655(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="4b280-123">For more information about writing applications in C# or Visual Basic .NET, see [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).</span></span>

<span data-ttu-id="4b280-124">Para obter mais informações sobre como criar aplicativos e scripts para o WMI, consulte:</span><span class="sxs-lookup"><span data-stu-id="4b280-124">For more information about creating applications and scripts for WMI, see:</span></span>

-   [<span data-ttu-id="4b280-125">Criando um aplicativo WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="4b280-125">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
-   [<span data-ttu-id="4b280-126">Criando um script WMI</span><span class="sxs-lookup"><span data-stu-id="4b280-126">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
-   [<span data-ttu-id="4b280-127">Criando um cliente WMI gerenciado</span><span class="sxs-lookup"><span data-stu-id="4b280-127">Creating a Managed WMI Client</span></span>](creating-a-managed-wmi-client.md)

<span data-ttu-id="4b280-128">Para executar a maioria das tarefas, use as [classes do WMI](wmi-classes.md)pré-instalado.</span><span class="sxs-lookup"><span data-stu-id="4b280-128">To perform most tasks, use the preinstalled [WMI classes](wmi-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b280-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b280-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b280-130">Usando o WMI</span><span class="sxs-lookup"><span data-stu-id="4b280-130">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
