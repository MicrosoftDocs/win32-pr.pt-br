---
description: Contém dados de conjunto de animação.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: CompressedAnimationSet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010256"
---
# <a name="compressedanimationset"></a><span data-ttu-id="330c5-103">CompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="330c5-103">CompressedAnimationSet</span></span>

<span data-ttu-id="330c5-104">Contém dados de conjunto de animação.</span><span class="sxs-lookup"><span data-stu-id="330c5-104">Contains animation set data.</span></span>

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

<span data-ttu-id="330c5-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="330c5-105">Where:</span></span>

-   <span data-ttu-id="330c5-106">CompressedBlockSize-tamanho total, em bytes, dos dados compactados no buffer de dados de animação do quadro chave compactado.</span><span class="sxs-lookup"><span data-stu-id="330c5-106">CompressedBlockSize - Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>
-   <span data-ttu-id="330c5-107">TicksPerSec-número de tiques de quadros-chave de animação que ocorrem por segundo.</span><span class="sxs-lookup"><span data-stu-id="330c5-107">TicksPerSec - Number of animation key frame ticks that occur per second.</span></span>
-   <span data-ttu-id="330c5-108">Reproduztype-tipo do loop de reprodução do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="330c5-108">PlaybackType - Type of the animation set playback loop.</span></span> <span data-ttu-id="330c5-109">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="330c5-109">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>
-   <span data-ttu-id="330c5-110">BufferLength-tamanho mínimo do buffer, em bytes, necessário para manter dados de animação de quadro chave compactados.</span><span class="sxs-lookup"><span data-stu-id="330c5-110">BufferLength - Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="330c5-111">Valor é igual a ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="330c5-111">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>
-   <span data-ttu-id="330c5-112">CompressedData \[ BufferLength \] -uma matriz de valores de dados compactados.</span><span class="sxs-lookup"><span data-stu-id="330c5-112">CompressedData\[BufferLength\] - An array of compressed data values.</span></span>

## <a name="see-also"></a><span data-ttu-id="330c5-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="330c5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330c5-114">Modelos</span><span class="sxs-lookup"><span data-stu-id="330c5-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="330c5-115">**XFILECOMPRESSEDANIMATIONSET**</span><span class="sxs-lookup"><span data-stu-id="330c5-115">**XFILECOMPRESSEDANIMATIONSET**</span></span>](xfilecompressedanimationset.md)
</dt> </dl>

 

 
