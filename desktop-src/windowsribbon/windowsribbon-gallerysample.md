---
title: Exemplo de galeria
description: este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da galeria incluídos na estrutura da faixa de Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691745"
---
# <a name="gallery-sample"></a><span data-ttu-id="5998c-103">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="5998c-103">Gallery Sample</span></span>

<span data-ttu-id="5998c-104">este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da galeria incluídos na estrutura da faixa de Windows.</span><span class="sxs-lookup"><span data-stu-id="5998c-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="5998c-105">O exemplo inclui código que pode ser usado para popular dinamicamente os itens nas galerias e manipular eventos de visualização de galeria especiais que dão suporte à interface do usuário orientada por resultados.</span><span class="sxs-lookup"><span data-stu-id="5998c-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

- [<span data-ttu-id="5998c-106">Usage</span><span class="sxs-lookup"><span data-stu-id="5998c-106">Usage</span></span>](#usage)
  - [<span data-ttu-id="5998c-107">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="5998c-107">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="5998c-108">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="5998c-108">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="5998c-109">Suporte</span><span class="sxs-lookup"><span data-stu-id="5998c-109">Support</span></span>](#support)
- [<span data-ttu-id="5998c-110">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="5998c-110">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="5998c-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5998c-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="5998c-112">Uso</span><span class="sxs-lookup"><span data-stu-id="5998c-112">Usage</span></span>

<span data-ttu-id="5998c-113">os exemplos da estrutura da faixa de Microsoft Visual Studio Windows podem ser baixados como projetos autônomos do [centro de Download da Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou instalados como parte do [SDK (Software Development Kit) do Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="5998c-113">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="5998c-114">Windows SDK (Software Development Kit) (caminho de instalação padrão):% programfiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ winui \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="5998c-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="5998c-115">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="5998c-115">Building the Sample</span></span>

<span data-ttu-id="5998c-116">Baixe o exemplo.</span><span class="sxs-lookup"><span data-stu-id="5998c-116">Download the sample.</span></span>

<span data-ttu-id="5998c-117">instale o SDK do Windows para Windows 7 e abra sua janela de comando de ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="5998c-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="5998c-118">No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="5998c-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="5998c-119">Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo.</span><span class="sxs-lookup"><span data-stu-id="5998c-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="5998c-120">No prompt de comando, digite MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="5998c-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="5998c-121">Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.</span><span class="sxs-lookup"><span data-stu-id="5998c-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="5998c-122">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="5998c-122">Running the Sample</span></span>

<span data-ttu-id="5998c-123">Para executar o exemplo na janela de comando compilar ambiente, execute o .exe arquivos na pasta de \\ depuração bin ou \\ Release bin contida na pasta de origem de exemplo.</span><span class="sxs-lookup"><span data-stu-id="5998c-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="5998c-124">Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.</span><span class="sxs-lookup"><span data-stu-id="5998c-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="5998c-125">Suporte</span><span class="sxs-lookup"><span data-stu-id="5998c-125">Support</span></span>

<span data-ttu-id="5998c-126">o [fórum de desenvolvimento da faixa de Windows da Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de.</span><span class="sxs-lookup"><span data-stu-id="5998c-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="5998c-127">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="5998c-127">Minimum Requirements</span></span>



| <span data-ttu-id="5998c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5998c-128">Requirement</span></span> | <span data-ttu-id="5998c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5998c-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5998c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5998c-130">Minimum supported client</span></span> | <span data-ttu-id="5998c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5998c-131">Windows 7</span></span><br/> <span data-ttu-id="5998c-132">Windows vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="5998c-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="5998c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5998c-133">Minimum supported server</span></span> | <span data-ttu-id="5998c-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5998c-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="5998c-135">Windows servidor 2008 com SP2 e [atualização de plataforma para o Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="5998c-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="5998c-136">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="5998c-136">Windows SDK</span></span>              | <span data-ttu-id="5998c-137">7.0</span><span class="sxs-lookup"><span data-stu-id="5998c-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="5998c-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5998c-138">Visual Studio</span></span>            | <span data-ttu-id="5998c-139">2008</span><span class="sxs-lookup"><span data-stu-id="5998c-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="5998c-140">Cabeçalhos e arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="5998c-140">Header and IDL files</span></span>     | <span data-ttu-id="5998c-141">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="5998c-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="5998c-142">a [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar Windows aplicativos de faixa de opções para o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5998c-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5998c-143">as atualizações de plataforma estarão disponíveis para todos os clientes Windows Vista e Windows Server 2008 por meio do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="5998c-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="5998c-144">aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5998c-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5998c-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5998c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5998c-146">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="5998c-146">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="5998c-147">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="5998c-147">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="5998c-148">Galeria suspensa</span><span class="sxs-lookup"><span data-stu-id="5998c-148">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="5998c-149">Galeria de faixa de bits</span><span class="sxs-lookup"><span data-stu-id="5998c-149">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="5998c-150">Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="5998c-150">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="5998c-151">Propriedades da coleção</span><span class="sxs-lookup"><span data-stu-id="5998c-151">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





