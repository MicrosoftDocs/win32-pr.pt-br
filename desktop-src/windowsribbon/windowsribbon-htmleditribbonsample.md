---
title: Exemplo de HTMLEditRibbon
description: este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo de MFC (MFC) existente para usar a faixa de Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: cfe75d13a69e0122766e51a00bcb1b15d52eab4e
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691705"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="55a91-103">Exemplo de HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="55a91-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="55a91-104">este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo de MFC (MFC) existente para usar a faixa de Windows.</span><span class="sxs-lookup"><span data-stu-id="55a91-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="55a91-105">ele foi criado por meio do aplicativo de exemplo MFC HTMLEdit existente e modificando seu código e recursos para usar a faixa de Windows.</span><span class="sxs-lookup"><span data-stu-id="55a91-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

- [<span data-ttu-id="55a91-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="55a91-106">Remarks</span></span>](#remarks)
- [<span data-ttu-id="55a91-107">Usage</span><span class="sxs-lookup"><span data-stu-id="55a91-107">Usage</span></span>](#usage)
  - [<span data-ttu-id="55a91-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="55a91-108">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="55a91-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="55a91-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="55a91-110">Suporte</span><span class="sxs-lookup"><span data-stu-id="55a91-110">Support</span></span>](#support)
- [<span data-ttu-id="55a91-111">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="55a91-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="55a91-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="55a91-112">Remarks</span></span>

<span data-ttu-id="55a91-113">Para o exemplo de MFC, consulte [exemplo de HtmlEdit: encapsula o controle de edição MSHTML do Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="55a91-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="55a91-114">Uso</span><span class="sxs-lookup"><span data-stu-id="55a91-114">Usage</span></span>

<span data-ttu-id="55a91-115">os exemplos da estrutura da faixa de Microsoft Visual Studio Windows podem ser baixados como projetos autônomos do [centro de Download da Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou instalados como parte do [SDK (Software Development Kit) do Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="55a91-115">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="55a91-116">Windows SDK (Software Development Kit) (caminho de instalação padrão):% programfiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ winui \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="55a91-116">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="55a91-117">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="55a91-117">Building the Sample</span></span>

<span data-ttu-id="55a91-118">Baixe o exemplo.</span><span class="sxs-lookup"><span data-stu-id="55a91-118">Download the sample.</span></span>

<span data-ttu-id="55a91-119">instale o SDK do Windows para Windows 7 e abra sua janela de comando de ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="55a91-119">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="55a91-120">No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="55a91-120">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="55a91-121">Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo.</span><span class="sxs-lookup"><span data-stu-id="55a91-121">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="55a91-122">No prompt de comando, digite MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="55a91-122">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="55a91-123">Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.</span><span class="sxs-lookup"><span data-stu-id="55a91-123">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="55a91-124">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="55a91-124">Running the Sample</span></span>

<span data-ttu-id="55a91-125">Para executar o exemplo na janela de comando compilar ambiente, execute o .exe arquivos na pasta de \\ depuração bin ou \\ Release bin contida na pasta de origem de exemplo.</span><span class="sxs-lookup"><span data-stu-id="55a91-125">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="55a91-126">Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.</span><span class="sxs-lookup"><span data-stu-id="55a91-126">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="55a91-127">Suporte</span><span class="sxs-lookup"><span data-stu-id="55a91-127">Support</span></span>

<span data-ttu-id="55a91-128">o [fórum de desenvolvimento da faixa de Windows da Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de.</span><span class="sxs-lookup"><span data-stu-id="55a91-128">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="55a91-129">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="55a91-129">Minimum Requirements</span></span>



| <span data-ttu-id="55a91-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="55a91-130">Requirement</span></span> | <span data-ttu-id="55a91-131">Valor</span><span class="sxs-lookup"><span data-stu-id="55a91-131">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a91-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55a91-132">Minimum supported client</span></span> | <span data-ttu-id="55a91-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="55a91-133">Windows 7</span></span><br/> <span data-ttu-id="55a91-134">Windows vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="55a91-134">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="55a91-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55a91-135">Minimum supported server</span></span> | <span data-ttu-id="55a91-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="55a91-136">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="55a91-137">Windows servidor 2008 com SP2 e [atualização de plataforma para o Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="55a91-137">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="55a91-138">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="55a91-138">Windows SDK</span></span>              | <span data-ttu-id="55a91-139">7.0</span><span class="sxs-lookup"><span data-stu-id="55a91-139">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="55a91-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55a91-140">Visual Studio</span></span>            | <span data-ttu-id="55a91-141">2008</span><span class="sxs-lookup"><span data-stu-id="55a91-141">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="55a91-142">Cabeçalhos e arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="55a91-142">Header and IDL files</span></span>     | <span data-ttu-id="55a91-143">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="55a91-143">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="55a91-144">a [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar Windows aplicativos de faixa de opções para o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="55a91-144">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="55a91-145">as atualizações de plataforma estarão disponíveis para todos os clientes Windows Vista e Windows Server 2008 por meio do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="55a91-145">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="55a91-146">aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="55a91-146">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





