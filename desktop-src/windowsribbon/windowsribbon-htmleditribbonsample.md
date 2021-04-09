---
title: Exemplo de HTMLEditRibbon
description: Este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo de MFC (MFC) existente para usar a faixa de, do Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009081"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="2a238-103">Exemplo de HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="2a238-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="2a238-104">Este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo de MFC (MFC) existente para usar a faixa de, do Windows.</span><span class="sxs-lookup"><span data-stu-id="2a238-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="2a238-105">Ele foi criado por meio do aplicativo de exemplo HTMLEdit do MFC existente e modificando seu código e recursos para usar a faixa de do Windows.</span><span class="sxs-lookup"><span data-stu-id="2a238-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

-   [<span data-ttu-id="2a238-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a238-106">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="2a238-107">Usage</span><span class="sxs-lookup"><span data-stu-id="2a238-107">Usage</span></span>](#usage)
    -   [<span data-ttu-id="2a238-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="2a238-108">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="2a238-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="2a238-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="2a238-110">Suporte</span><span class="sxs-lookup"><span data-stu-id="2a238-110">Support</span></span>](#support)
-   [<span data-ttu-id="2a238-111">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="2a238-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="2a238-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a238-112">Remarks</span></span>

<span data-ttu-id="2a238-113">Para o exemplo de MFC, consulte [exemplo de HtmlEdit: encapsula o controle de edição MSHTML do Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="2a238-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="2a238-114">Uso</span><span class="sxs-lookup"><span data-stu-id="2a238-114">Usage</span></span>

<span data-ttu-id="2a238-115">O exemplo de HTMLEditRibbon pode ser baixado como um projeto de Microsoft Visual Studio autônomo do [centro de download da Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou instalado como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2a238-115">The HTMLEditRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="2a238-116">Centro de download da Microsoft: [exemplos de faixa](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en) de medida do Windows</span><span class="sxs-lookup"><span data-stu-id="2a238-116">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="2a238-117">SDK (Software Development Kit) do Windows (caminho de instalação padrão):% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ WinUI \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="2a238-117">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="2a238-118">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="2a238-118">Building the Sample</span></span>

<span data-ttu-id="2a238-119">Baixe o exemplo no seu disco rígido.</span><span class="sxs-lookup"><span data-stu-id="2a238-119">Download the sample to your hard disk.</span></span>

<span data-ttu-id="2a238-120">Instale o SDK do Windows para o Windows 7 e abra sua janela de comando de ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="2a238-120">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="2a238-121">No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="2a238-121">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="2a238-122">Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo.</span><span class="sxs-lookup"><span data-stu-id="2a238-122">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="2a238-123">No prompt de comando, digite MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="2a238-123">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="2a238-124">Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.</span><span class="sxs-lookup"><span data-stu-id="2a238-124">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="2a238-125">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="2a238-125">Running the Sample</span></span>

<span data-ttu-id="2a238-126">Para executar o exemplo na janela de comando compilar ambiente, execute os arquivos. exe na pasta de \\ depuração bin ou \\ solte contida na pasta de origem de exemplo.</span><span class="sxs-lookup"><span data-stu-id="2a238-126">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="2a238-127">Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.</span><span class="sxs-lookup"><span data-stu-id="2a238-127">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="2a238-128">Suporte</span><span class="sxs-lookup"><span data-stu-id="2a238-128">Support</span></span>

<span data-ttu-id="2a238-129">O [Fórum de desenvolvimento da faixa](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de Dasgem do Windows está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de de uma Windows.</span><span class="sxs-lookup"><span data-stu-id="2a238-129">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="2a238-130">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="2a238-130">Minimum Requirements</span></span>



| <span data-ttu-id="2a238-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a238-131">Requirement</span></span> | <span data-ttu-id="2a238-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2a238-132">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a238-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a238-133">Minimum supported client</span></span> | <span data-ttu-id="2a238-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2a238-134">Windows 7</span></span><br/> <span data-ttu-id="2a238-135">Windows Vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a238-135">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="2a238-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a238-136">Minimum supported server</span></span> | <span data-ttu-id="2a238-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a238-137">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="2a238-138">Windows Server 2008 com SP2 e [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a238-138">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="2a238-139">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="2a238-139">Windows SDK</span></span>              | <span data-ttu-id="2a238-140">7.0</span><span class="sxs-lookup"><span data-stu-id="2a238-140">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="2a238-141">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2a238-141">Visual Studio</span></span>            | <span data-ttu-id="2a238-142">2008</span><span class="sxs-lookup"><span data-stu-id="2a238-142">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="2a238-143">Cabeçalhos e arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="2a238-143">Header and IDL files</span></span>     | <span data-ttu-id="2a238-144">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="2a238-144">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="2a238-145">A [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar aplicativos de faixa de opções do Windows para o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2a238-145">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="2a238-146">As atualizações de plataforma estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="2a238-146">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="2a238-147">Aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2a238-147">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





