---
title: Exemplo de DropDownColorPicker
description: Este exemplo de código demonstra a marcação e o código necessários para usar um controle DropDownColorPicker da faixa de dasgem do Windows.
ms.assetid: cc8e18a6-9ed5-47ca-a807-f50838821f14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000db12fbc3b3f7ace679e4e8b1f4756d59f6e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085641"
---
# <a name="dropdowncolorpicker-sample"></a><span data-ttu-id="38e43-103">Exemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="38e43-103">DropDownColorPicker Sample</span></span>

<span data-ttu-id="38e43-104">Este exemplo de código demonstra a marcação e o código necessários para usar um controle DropDownColorPicker da faixa de dasgem do Windows.</span><span class="sxs-lookup"><span data-stu-id="38e43-104">This code sample demonstrates the markup and code required to use a Windows Ribbon DropDownColorPicker control.</span></span>

-   [<span data-ttu-id="38e43-105">Usage</span><span class="sxs-lookup"><span data-stu-id="38e43-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="38e43-106">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38e43-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="38e43-107">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38e43-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="38e43-108">Suporte</span><span class="sxs-lookup"><span data-stu-id="38e43-108">Support</span></span>](#support)
-   [<span data-ttu-id="38e43-109">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="38e43-109">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="38e43-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38e43-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="38e43-111">Uso</span><span class="sxs-lookup"><span data-stu-id="38e43-111">Usage</span></span>

<span data-ttu-id="38e43-112">O exemplo de DropDownColorPicker pode ser baixado como um projeto de Microsoft Visual Studio autônomo do [centro de download da Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou instalado como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="38e43-112">The DropDownColorPicker Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="38e43-113">Centro de download da Microsoft: [exemplos de faixa](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en) de medida do Windows</span><span class="sxs-lookup"><span data-stu-id="38e43-113">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="38e43-114">SDK (Software Development Kit) do Windows (caminho de instalação padrão):% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ WinUI \\ WindowsRibbon \\ DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="38e43-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\DropDownColorPicker</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="38e43-115">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38e43-115">Building the Sample</span></span>

<span data-ttu-id="38e43-116">Baixe o exemplo no seu disco rígido.</span><span class="sxs-lookup"><span data-stu-id="38e43-116">Download the sample to your hard disk.</span></span>

<span data-ttu-id="38e43-117">Instale o SDK do Windows para o Windows 7 e abra sua janela de comando de ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="38e43-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="38e43-118">No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="38e43-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="38e43-119">Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo.</span><span class="sxs-lookup"><span data-stu-id="38e43-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="38e43-120">No prompt de comando, digite MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="38e43-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="38e43-121">Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.</span><span class="sxs-lookup"><span data-stu-id="38e43-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="38e43-122">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38e43-122">Running the Sample</span></span>

<span data-ttu-id="38e43-123">Para executar o exemplo na janela de comando compilar ambiente, execute os arquivos. exe na pasta de \\ depuração bin ou \\ solte contida na pasta de origem de exemplo.</span><span class="sxs-lookup"><span data-stu-id="38e43-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="38e43-124">Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.</span><span class="sxs-lookup"><span data-stu-id="38e43-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="38e43-125">Suporte</span><span class="sxs-lookup"><span data-stu-id="38e43-125">Support</span></span>

<span data-ttu-id="38e43-126">O [Fórum de desenvolvimento da faixa](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de Dasgem do Windows está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de de uma Windows.</span><span class="sxs-lookup"><span data-stu-id="38e43-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="38e43-127">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="38e43-127">Minimum Requirements</span></span>



| <span data-ttu-id="38e43-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="38e43-128">Requirement</span></span> | <span data-ttu-id="38e43-129">Valor</span><span class="sxs-lookup"><span data-stu-id="38e43-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e43-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38e43-130">Minimum supported client</span></span> | <span data-ttu-id="38e43-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38e43-131">Windows 7</span></span><br/> <span data-ttu-id="38e43-132">Windows Vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="38e43-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="38e43-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38e43-133">Minimum supported server</span></span> | <span data-ttu-id="38e43-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38e43-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="38e43-135">Windows Server 2008 com SP2 e [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="38e43-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="38e43-136">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="38e43-136">Windows SDK</span></span>              | <span data-ttu-id="38e43-137">7.0</span><span class="sxs-lookup"><span data-stu-id="38e43-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="38e43-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="38e43-138">Visual Studio</span></span>            | <span data-ttu-id="38e43-139">2008</span><span class="sxs-lookup"><span data-stu-id="38e43-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="38e43-140">Cabeçalhos e arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="38e43-140">Header and IDL files</span></span>     | <span data-ttu-id="38e43-141">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="38e43-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="38e43-142">A [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar aplicativos de faixa de opções do Windows para o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="38e43-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="38e43-143">As atualizações de plataforma estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="38e43-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="38e43-144">Aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="38e43-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="38e43-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38e43-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38e43-146">Seletor de cores suspensa</span><span class="sxs-lookup"><span data-stu-id="38e43-146">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="38e43-147">Propriedades do seletor de cores</span><span class="sxs-lookup"><span data-stu-id="38e43-147">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 





