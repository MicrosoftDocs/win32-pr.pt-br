---
description: Vsdiagview e Vssagent são ferramentas que você pode usar para solucionar problemas de aplicativos VSS. Observe que essas ferramentas estão incluídas no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Usando diagnósticos do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794550"
---
# <a name="using-vss-diagnostics"></a><span data-ttu-id="f4f66-103">Usando diagnósticos do VSS</span><span class="sxs-lookup"><span data-stu-id="f4f66-103">Using VSS Diagnostics</span></span>

<span data-ttu-id="f4f66-104">Vsdiagview e Vssagent são ferramentas que você pode usar para solucionar problemas de aplicativos VSS.</span><span class="sxs-lookup"><span data-stu-id="f4f66-104">Vsdiagview and Vssagent are tools that you can use to troubleshoot VSS applications.</span></span>

> [!Note]  
> <span data-ttu-id="f4f66-105">Essas ferramentas estão incluídas no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="f4f66-105">These tools are included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="f4f66-106">Você pode baixar o SDK do Windows do [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f4f66-106">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="f4f66-107">Na instalação do SDK do Windows, essas ferramentas podem ser encontradas em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para o Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para o windows de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="f4f66-107">In the Windows SDK installation, these tools can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="gathering-data"></a><span data-ttu-id="f4f66-108">Coletando dados</span><span class="sxs-lookup"><span data-stu-id="f4f66-108">Gathering Data</span></span>

<span data-ttu-id="f4f66-109">Você pode coletar dados usando o comando Vssagent.</span><span class="sxs-lookup"><span data-stu-id="f4f66-109">You can gather data by using the Vssagent command.</span></span>

<span data-ttu-id="f4f66-110">**Para coletar dados usando o Vssagent**</span><span class="sxs-lookup"><span data-stu-id="f4f66-110">**To gather data using Vssagent**</span></span>

1.  <span data-ttu-id="f4f66-111">Para coletar dados da linha de comando, use o comando Vssagent da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f4f66-111">To gather data from the command line, use the Vssagent command as follows:</span></span>

    <span data-ttu-id="f4f66-112">**vssagent-coletar** *xmlFileName \* \* *. xml**</span><span class="sxs-lookup"><span data-stu-id="f4f66-112">**vssagent -gather** *XmlFileName\*\*\*.xml*\*</span></span>

2.  <span data-ttu-id="f4f66-113">Para exibir o arquivo de saída, consulte a seção exibindo dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4f66-113">To view the output file, see the following Viewing Data section.</span></span>

## <a name="viewing-data"></a><span data-ttu-id="f4f66-114">Exibindo dados</span><span class="sxs-lookup"><span data-stu-id="f4f66-114">Viewing Data</span></span>

<span data-ttu-id="f4f66-115">O aplicativo Vsdiagview pode ser usado para exibir dados que foram coletados usando o comando Vssagent.</span><span class="sxs-lookup"><span data-stu-id="f4f66-115">The Vsdiagview application can be used to view data that was gathered by using the Vssagent command.</span></span> <span data-ttu-id="f4f66-116">Vsdiagview exibe as seguintes informações sobre o computador:</span><span class="sxs-lookup"><span data-stu-id="f4f66-116">Vsdiagview displays the following information about the computer:</span></span>

-   <span data-ttu-id="f4f66-117">Informações sobre o computador, como a versão do sistema operacional, a memória total disponível e a velocidade da CPU</span><span class="sxs-lookup"><span data-stu-id="f4f66-117">Information about the computer, such as the operating system version, total available memory, and CPU speed</span></span>
-   <span data-ttu-id="f4f66-118">Os nomes e os números de versão dos binários do VSS</span><span class="sxs-lookup"><span data-stu-id="f4f66-118">The names and version numbers of the VSS binaries</span></span>
-   <span data-ttu-id="f4f66-119">Os nomes e as propriedades dos dispositivos de disco e volume</span><span class="sxs-lookup"><span data-stu-id="f4f66-119">The names and properties of the disk and volume devices</span></span>
-   <span data-ttu-id="f4f66-120">Os nomes e as propriedades de qualquer aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="f4f66-120">The names and properties of any COM+ applications</span></span>
-   <span data-ttu-id="f4f66-121">Os nomes dos logs de eventos que podem ser usados para diagnosticar problemas de VSS</span><span class="sxs-lookup"><span data-stu-id="f4f66-121">The names of event logs that can be used for diagnosing VSS problems</span></span>
-   <span data-ttu-id="f4f66-122">Os nomes de qualquer gravador VSS e os eventos que eles manipulam</span><span class="sxs-lookup"><span data-stu-id="f4f66-122">The names of any VSS writers and the events that they handle</span></span>
-   <span data-ttu-id="f4f66-123">Informações sobre outros arquivos do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f4f66-123">Information about other operating system files</span></span>

<span data-ttu-id="f4f66-124">**Para exibir dados usando o Vsdiagview**</span><span class="sxs-lookup"><span data-stu-id="f4f66-124">**To view data using Vsdiagview**</span></span>

1.  <span data-ttu-id="f4f66-125">No menu arquivo, escolha **abrir** para procurar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f4f66-125">In the File menu, choose **Open** to browse for a file.</span></span> <span data-ttu-id="f4f66-126">(O local padrão é C: \\ vssdiag.)</span><span class="sxs-lookup"><span data-stu-id="f4f66-126">(The default location is C:\\vssdiag.)</span></span>
2.  <span data-ttu-id="f4f66-127">Clique em **abrir** para exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="f4f66-127">Click **Open** to view the data.</span></span>

 

 



