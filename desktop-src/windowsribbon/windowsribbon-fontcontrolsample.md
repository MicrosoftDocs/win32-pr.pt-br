---
title: Exemplo de FontControl
description: este exemplo de código demonstra a marcação e o código necessários para implementar um FontControl em um aplicativo de faixa de Windows.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 52a81a1a1950305437a7bbc68aab95876b3a6374
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691755"
---
# <a name="fontcontrol-sample"></a><span data-ttu-id="e698b-103">Exemplo de FontControl</span><span class="sxs-lookup"><span data-stu-id="e698b-103">FontControl Sample</span></span>

<span data-ttu-id="e698b-104">este exemplo de código demonstra a marcação e o código necessários para implementar um FontControl em um aplicativo de faixa de Windows.</span><span class="sxs-lookup"><span data-stu-id="e698b-104">This code sample demonstrates the markup and code required to implement a FontControl within a Windows Ribbon application.</span></span>

- [<span data-ttu-id="e698b-105">Usage</span><span class="sxs-lookup"><span data-stu-id="e698b-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="e698b-106">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e698b-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="e698b-107">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e698b-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="e698b-108">Suporte</span><span class="sxs-lookup"><span data-stu-id="e698b-108">Support</span></span>](#support)
- [<span data-ttu-id="e698b-109">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="e698b-109">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="e698b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e698b-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="e698b-111">Uso</span><span class="sxs-lookup"><span data-stu-id="e698b-111">Usage</span></span>

<span data-ttu-id="e698b-112">os exemplos da estrutura da faixa de Microsoft Visual Studio Windows podem ser baixados como projetos autônomos do [centro de Download da Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou instalados como parte do [SDK (Software Development Kit) do Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="e698b-112">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="e698b-113">Windows SDK (Software Development Kit) (caminho de instalação padrão):% programfiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ winui \\ WindowsRibbon \\ FontControl</span><span class="sxs-lookup"><span data-stu-id="e698b-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\FontControl</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="e698b-114">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e698b-114">Building the Sample</span></span>

<span data-ttu-id="e698b-115">Baixe o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e698b-115">Download the sample.</span></span>

<span data-ttu-id="e698b-116">instale o SDK do Windows para Windows 7 e abra sua janela de comando de ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="e698b-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="e698b-117">No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="e698b-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="e698b-118">Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo.</span><span class="sxs-lookup"><span data-stu-id="e698b-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="e698b-119">No prompt de comando, digite MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="e698b-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="e698b-120">Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.</span><span class="sxs-lookup"><span data-stu-id="e698b-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="e698b-121">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e698b-121">Running the Sample</span></span>

<span data-ttu-id="e698b-122">Para executar o exemplo na janela de comando compilar ambiente, execute o .exe arquivos na pasta de \\ depuração bin ou \\ Release bin contida na pasta de origem de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e698b-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="e698b-123">Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.</span><span class="sxs-lookup"><span data-stu-id="e698b-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="e698b-124">Suporte</span><span class="sxs-lookup"><span data-stu-id="e698b-124">Support</span></span>

<span data-ttu-id="e698b-125">o [fórum de desenvolvimento da faixa de Windows da Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de.</span><span class="sxs-lookup"><span data-stu-id="e698b-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="e698b-126">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="e698b-126">Minimum Requirements</span></span>



| <span data-ttu-id="e698b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e698b-127">Requirement</span></span> | <span data-ttu-id="e698b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e698b-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e698b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e698b-129">Minimum supported client</span></span> | <span data-ttu-id="e698b-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e698b-130">Windows 7</span></span><br/> <span data-ttu-id="e698b-131">Windows vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e698b-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="e698b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e698b-132">Minimum supported server</span></span> | <span data-ttu-id="e698b-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e698b-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="e698b-134">Windows servidor 2008 com SP2 e [atualização de plataforma para o Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e698b-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="e698b-135">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="e698b-135">Windows SDK</span></span>              | <span data-ttu-id="e698b-136">7.0</span><span class="sxs-lookup"><span data-stu-id="e698b-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="e698b-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e698b-137">Visual Studio</span></span>            | <span data-ttu-id="e698b-138">2008</span><span class="sxs-lookup"><span data-stu-id="e698b-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="e698b-139">Cabeçalhos e arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="e698b-139">Header and IDL files</span></span>     | <span data-ttu-id="e698b-140">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="e698b-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="e698b-141">a [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar Windows aplicativos de faixa de opções para o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e698b-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e698b-142">as atualizações de plataforma estarão disponíveis para todos os clientes Windows Vista e Windows Server 2008 por meio do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e698b-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="e698b-143">aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e698b-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e698b-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e698b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e698b-145">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="e698b-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="e698b-146">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="e698b-146">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





