---
title: Instalando visualizações
description: Instalando visualizações
ms.assetid: ca391e38-def5-47da-81f7-94aa96530387
keywords:
- Plug-ins do Windows Media Player, visualizações
- plug-ins, visualizações
- visualizações, instalando
- visualizações personalizadas, instalando
- Instalando visualizações
- visualizações, registrando
- visualizações personalizadas, registrando
- registro, visualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1dc8f33d7b5f5b938bee6c89d946955509ab34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800126"
---
# <a name="installing-visualizations"></a><span data-ttu-id="bae77-111">Instalando visualizações</span><span class="sxs-lookup"><span data-stu-id="bae77-111">Installing Visualizations</span></span>

<span data-ttu-id="bae77-112">Você deve fornecer um processo de instalação para o usuário da sua visualização.</span><span class="sxs-lookup"><span data-stu-id="bae77-112">You must provide an installation process for the user of your visualization.</span></span> <span data-ttu-id="bae77-113">Você também deve fornecer um processo de desinstalação para o usuário.</span><span class="sxs-lookup"><span data-stu-id="bae77-113">You must also provide an uninstall process for the user.</span></span> <span data-ttu-id="bae77-114">A versão atual do Windows Media Player não instala visualizações da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bae77-114">The current version of Windows Media Player does not install visualizations from the user interface.</span></span>

## <a name="installing-to-the-visualization-folder"></a><span data-ttu-id="bae77-115">Instalando na pasta de visualização</span><span class="sxs-lookup"><span data-stu-id="bae77-115">Installing to the Visualization Folder</span></span>

<span data-ttu-id="bae77-116">É recomendável que você instale todas as visualizações na subpasta visualizações da pasta em que o Windows Media Player está instalado.</span><span class="sxs-lookup"><span data-stu-id="bae77-116">It is recommended that you install all visualizations in the Visualizations subfolder of the folder where Windows Media Player is installed.</span></span>

## <a name="registering-your-visualization"></a><span data-ttu-id="bae77-117">Registrando sua visualização</span><span class="sxs-lookup"><span data-stu-id="bae77-117">Registering Your Visualization</span></span>

<span data-ttu-id="bae77-118">As visualizações são DLLs COM e seguem todas as regras normais de instalação e remoção.</span><span class="sxs-lookup"><span data-stu-id="bae77-118">Visualizations are COM DLLs and follow all the normal rules of installation and removal.</span></span> <span data-ttu-id="bae77-119">Você pode usar regsvr32.exe ou outras ferramentas de instalação para registrar sua visualização.</span><span class="sxs-lookup"><span data-stu-id="bae77-119">You can use regsvr32.exe or other installation tools to register your visualization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bae77-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bae77-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae77-121">**Sobre visualizações personalizadas**</span><span class="sxs-lookup"><span data-stu-id="bae77-121">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




