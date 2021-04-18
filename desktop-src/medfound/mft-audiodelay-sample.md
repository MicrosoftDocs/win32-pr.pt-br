---
description: Exemplo de AudioDelay de MFT \_
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Exemplo de MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753050"
---
# <a name="mft_audiodelay-sample"></a><span data-ttu-id="67529-103">Exemplo de AudioDelay de MFT \_</span><span class="sxs-lookup"><span data-stu-id="67529-103">MFT\_AudioDelay Sample</span></span>

<span data-ttu-id="67529-104">Mostra como implementar um efeito de áudio como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="67529-104">Shows how to implement an audio effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="67529-105">A MFT de atraso de áudio aceita áudio PCM como entrada, aplica um efeito de atraso (eco) e gera os dados de áudio modificados.</span><span class="sxs-lookup"><span data-stu-id="67529-105">The audio delay MFT accepts PCM audio as input, applies a delay (echo) effect, and outputs the modified audio data.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="67529-106">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="67529-106">APIs Demonstrated</span></span>

<span data-ttu-id="67529-107">Este exemplo demonstra as seguintes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="67529-107">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="67529-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="67529-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="67529-109">Uso</span><span class="sxs-lookup"><span data-stu-id="67529-109">Usage</span></span>

<span data-ttu-id="67529-110">O \_ exemplo AudioDelay de MFT cria uma DLL que é um servidor com para o MFT.</span><span class="sxs-lookup"><span data-stu-id="67529-110">The MFT\_AudioDelay sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="67529-111">Antes de usar o MFT, você deve registrar a DLL.</span><span class="sxs-lookup"><span data-stu-id="67529-111">Before using the MFT, you must register the DLL.</span></span> <span data-ttu-id="67529-112">Você pode usar a ferramenta TopoEdit para criar uma topologia que inclui a MFT de atraso de áudio.</span><span class="sxs-lookup"><span data-stu-id="67529-112">You can use the TopoEdit tool to build a topology that includes the audio delay MFT.</span></span> <span data-ttu-id="67529-113">Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="67529-113">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span> <span data-ttu-id="67529-114">Você também pode modificar o [exemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)) para usar o MFT.</span><span class="sxs-lookup"><span data-stu-id="67529-114">You can also modify the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)) to use the MFT.</span></span> <span data-ttu-id="67529-115">Será necessário modificar a função AddBranchToPartialTopology no Player. cpp.</span><span class="sxs-lookup"><span data-stu-id="67529-115">You will need to modify the AddBranchToPartialTopology function in Player.cpp.</span></span> <span data-ttu-id="67529-116">Altere a seguinte linha de:</span><span class="sxs-lookup"><span data-stu-id="67529-116">Change the following line from:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

<span data-ttu-id="67529-117">Para:</span><span class="sxs-lookup"><span data-stu-id="67529-117">To:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

<span data-ttu-id="67529-118">O valor CLSID \_ DelayMFT é declarado no arquivo de cabeçalho AudioDelayUuids. h na pasta de \_ exemplo MFT AudioDelay.</span><span class="sxs-lookup"><span data-stu-id="67529-118">The value CLSID\_DelayMFT is declared in the header file AudioDelayUuids.h in the MFT\_AudioDelay sample folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="67529-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67529-119">Requirements</span></span>



| <span data-ttu-id="67529-120">Produto</span><span class="sxs-lookup"><span data-stu-id="67529-120">Product</span></span>                                                        | <span data-ttu-id="67529-121">Versão</span><span class="sxs-lookup"><span data-stu-id="67529-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="67529-122">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="67529-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="67529-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="67529-123">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="67529-124">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="67529-124">Downloading the Sample</span></span>

<span data-ttu-id="67529-125">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span><span class="sxs-lookup"><span data-stu-id="67529-125">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67529-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67529-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67529-127">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67529-127">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="67529-128">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67529-128">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="67529-129">Exemplo de escala de cinza da MFT \_</span><span class="sxs-lookup"><span data-stu-id="67529-129">MFT\_Grayscale Sample</span></span>](mft-grayscale-sample.md)
</dt> <dt>

[<span data-ttu-id="67529-130">Gravando uma MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="67529-130">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
