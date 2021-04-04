---
title: Exemplo de galeria
description: Este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da Galeria incluídos na estrutura da faixa de tipos do Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085294"
---
# <a name="gallery-sample"></a><span data-ttu-id="3a104-103">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="3a104-103">Gallery Sample</span></span>

<span data-ttu-id="3a104-104">Este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da Galeria incluídos na estrutura da faixa de tipos do Windows.</span><span class="sxs-lookup"><span data-stu-id="3a104-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="3a104-105">O exemplo inclui código que pode ser usado para popular dinamicamente os itens nas galerias e manipular eventos de visualização de galeria especiais que dão suporte à interface do usuário orientada por resultados.</span><span class="sxs-lookup"><span data-stu-id="3a104-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

-   [<span data-ttu-id="3a104-106">Usage</span><span class="sxs-lookup"><span data-stu-id="3a104-106">Usage</span></span>](#usage)
    -   [<span data-ttu-id="3a104-107">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3a104-107">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="3a104-108">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3a104-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="3a104-109">Suporte</span><span class="sxs-lookup"><span data-stu-id="3a104-109">Support</span></span>](#support)
-   [<span data-ttu-id="3a104-110">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="3a104-110">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="3a104-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a104-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="3a104-112">Uso</span><span class="sxs-lookup"><span data-stu-id="3a104-112">Usage</span></span>

<span data-ttu-id="3a104-113">O exemplo de galeria pode ser baixado como um projeto de Microsoft Visual Studio autônomo do [centro de download da Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou instalado como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a104-113">The Gallery Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="3a104-114">Centro de download da Microsoft: [exemplos de faixa](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en) de medida do Windows</span><span class="sxs-lookup"><span data-stu-id="3a104-114">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="3a104-115">SDK (Software Development Kit) do Windows (caminho de instalação padrão):% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ WinUI \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="3a104-115">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="3a104-116">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3a104-116">Building the Sample</span></span>

<span data-ttu-id="3a104-117">Baixe o exemplo no seu disco rígido.</span><span class="sxs-lookup"><span data-stu-id="3a104-117">Download the sample to your hard disk.</span></span>

<span data-ttu-id="3a104-118">Instale o SDK do Windows para o Windows 7 e abra sua janela de comando de ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="3a104-118">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="3a104-119">No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="3a104-119">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="3a104-120">Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo.</span><span class="sxs-lookup"><span data-stu-id="3a104-120">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="3a104-121">No prompt de comando, digite MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="3a104-121">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="3a104-122">Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.</span><span class="sxs-lookup"><span data-stu-id="3a104-122">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="3a104-123">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3a104-123">Running the Sample</span></span>

<span data-ttu-id="3a104-124">Para executar o exemplo na janela de comando compilar ambiente, execute os arquivos. exe na pasta de \\ depuração bin ou \\ solte contida na pasta de origem de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3a104-124">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="3a104-125">Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.</span><span class="sxs-lookup"><span data-stu-id="3a104-125">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="3a104-126">Suporte</span><span class="sxs-lookup"><span data-stu-id="3a104-126">Support</span></span>

<span data-ttu-id="3a104-127">O [Fórum de desenvolvimento da faixa](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de Dasgem do Windows está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de de uma Windows.</span><span class="sxs-lookup"><span data-stu-id="3a104-127">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="3a104-128">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="3a104-128">Minimum Requirements</span></span>



| <span data-ttu-id="3a104-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a104-129">Requirement</span></span> | <span data-ttu-id="3a104-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3a104-130">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a104-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a104-131">Minimum supported client</span></span> | <span data-ttu-id="3a104-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a104-132">Windows 7</span></span><br/> <span data-ttu-id="3a104-133">Windows Vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a104-133">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="3a104-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a104-134">Minimum supported server</span></span> | <span data-ttu-id="3a104-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3a104-135">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="3a104-136">Windows Server 2008 com SP2 e [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a104-136">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="3a104-137">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="3a104-137">Windows SDK</span></span>              | <span data-ttu-id="3a104-138">7.0</span><span class="sxs-lookup"><span data-stu-id="3a104-138">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="3a104-139">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3a104-139">Visual Studio</span></span>            | <span data-ttu-id="3a104-140">2008</span><span class="sxs-lookup"><span data-stu-id="3a104-140">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="3a104-141">Cabeçalhos e arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="3a104-141">Header and IDL files</span></span>     | <span data-ttu-id="3a104-142">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="3a104-142">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="3a104-143">A [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar aplicativos de faixa de opções do Windows para o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3a104-143">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="3a104-144">As atualizações de plataforma estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="3a104-144">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="3a104-145">Aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3a104-145">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3a104-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a104-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a104-147">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="3a104-147">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="3a104-148">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="3a104-148">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="3a104-149">Galeria suspensa</span><span class="sxs-lookup"><span data-stu-id="3a104-149">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="3a104-150">Galeria de faixa de bits</span><span class="sxs-lookup"><span data-stu-id="3a104-150">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="3a104-151">Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="3a104-151">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="3a104-152">Propriedades da coleção</span><span class="sxs-lookup"><span data-stu-id="3a104-152">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





