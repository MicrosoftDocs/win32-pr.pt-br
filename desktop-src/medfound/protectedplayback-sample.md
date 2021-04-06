---
description: Mostra como reproduzir conteúdo de mídia protegido no Microsoft Media Foundation.
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: Exemplo de ProtectedPlayback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee64b2a64ce4d40b6f15c2e5afb3b9a39e84c619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647750"
---
# <a name="protectedplayback-sample"></a><span data-ttu-id="bd8f8-103">Exemplo de ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="bd8f8-103">ProtectedPlayback Sample</span></span>

<span data-ttu-id="bd8f8-104">Mostra como reproduzir conteúdo de mídia protegido no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="bd8f8-104">Shows how to play protected media content in Microsoft Media Foundation.</span></span>

## <a name="usage"></a><span data-ttu-id="bd8f8-105">Uso</span><span class="sxs-lookup"><span data-stu-id="bd8f8-105">Usage</span></span>

<span data-ttu-id="bd8f8-106">O exemplo ProtectedPlayback cria um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="bd8f8-106">The ProtectedPlayback sample builds a Windows application.</span></span>

<span data-ttu-id="bd8f8-107">Para reproduzir um arquivo de mídia local, selecione **Abrir arquivo** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="bd8f8-107">To play a local media file, select **Open File** from the **File** menu.</span></span> <span data-ttu-id="bd8f8-108">Para especificar um arquivo por URL, selecione **abrir URL** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="bd8f8-108">To specify a file by URL, select **Open URL** from the **File** menu.</span></span> <span data-ttu-id="bd8f8-109">Depois de selecionar um arquivo, a reprodução é iniciada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bd8f8-109">After you select a file, playback begins automatically.</span></span> <span data-ttu-id="bd8f8-110">Para pausar a reprodução, pressione a barra de espaços.</span><span class="sxs-lookup"><span data-stu-id="bd8f8-110">To pause playback, press the SPACEBAR.</span></span> <span data-ttu-id="bd8f8-111">Para retomar a reprodução, pressione a barra de espaços novamente.</span><span class="sxs-lookup"><span data-stu-id="bd8f8-111">To resume playback, press the SPACEBAR again.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="bd8f8-112">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="bd8f8-112">APIs Demonstrated</span></span>

<span data-ttu-id="bd8f8-113">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="bd8f8-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="bd8f8-114">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="bd8f8-114">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [<span data-ttu-id="bd8f8-115">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="bd8f8-115">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a><span data-ttu-id="bd8f8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd8f8-116">Requirements</span></span>



| <span data-ttu-id="bd8f8-117">Produto</span><span class="sxs-lookup"><span data-stu-id="bd8f8-117">Product</span></span>                                                        | <span data-ttu-id="bd8f8-118">Versão</span><span class="sxs-lookup"><span data-stu-id="bd8f8-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="bd8f8-119">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="bd8f8-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bd8f8-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd8f8-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bd8f8-121">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bd8f8-121">Downloading the Sample</span></span>

<span data-ttu-id="bd8f8-122">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span><span class="sxs-lookup"><span data-stu-id="bd8f8-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd8f8-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd8f8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd8f8-124">Como reproduzir arquivos de mídia protegidos</span><span class="sxs-lookup"><span data-stu-id="bd8f8-124">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="bd8f8-125">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd8f8-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

<span data-ttu-id="bd8f8-126">[Exemplo de MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd8f8-126">[MFPlayer Sample](/previous-versions//bb970516(v=vs.85))</span></span>
</dt> </dl>

 

 
