---
description: O método Zoom amplia a exibição de vídeo para dentro ou para fora, centralizado em um determinado conjunto de coordenadas de tela.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Método de zoom
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461289"
---
# <a name="zoom-method"></a><span data-ttu-id="1f19f-103">Método de zoom</span><span class="sxs-lookup"><span data-stu-id="1f19f-103">Zoom Method</span></span>

> [!Note]  
> <span data-ttu-id="1f19f-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f19f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1f19f-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1f19f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1f19f-106">O `Zoom` método amplia a exibição de vídeo para dentro ou para fora, centralizado em um determinado conjunto de coordenadas de tela.</span><span class="sxs-lookup"><span data-stu-id="1f19f-106">The `Zoom` method zooms the video display in or out, centered on a given set of screen coordinates.</span></span>

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a><span data-ttu-id="1f19f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f19f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f19f-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span><span class="sxs-lookup"><span data-stu-id="1f19f-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span></span>
</dt> <dd>

<span data-ttu-id="1f19f-109">Especifica a coordenada x no centro da área de zoom retangular como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="1f19f-109">Specifies the x-coordinate at the center of the rectangular zoom area as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="1f19f-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span><span class="sxs-lookup"><span data-stu-id="1f19f-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span></span>
</dt> <dd>

<span data-ttu-id="1f19f-111">Especifica a coordenada y no centro do retângulo a ser ampliado como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="1f19f-111">Specifies the y-coordinate at the center of the rectangle to be zoomed as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="1f19f-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span><span class="sxs-lookup"><span data-stu-id="1f19f-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span></span>
</dt> <dd>

<span data-ttu-id="1f19f-113">Especifica o fator de ampliação aplicado ao valor de zoom atual como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="1f19f-113">Specifies the magnification factor applied to the current zoom value as an Integer.</span></span> <span data-ttu-id="1f19f-114">O valor máximo total depende do que a sobreposição de hardware pode dar suporte; Normalmente, isso é um fator de 32 a 64 vezes o tamanho original.</span><span class="sxs-lookup"><span data-stu-id="1f19f-114">The total maximum value depends on what the hardware overlay can support; this is typically a factor of 32 to 64 times the original size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f19f-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1f19f-115">Return Value</span></span>

<span data-ttu-id="1f19f-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1f19f-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f19f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f19f-117">Remarks</span></span>

<span data-ttu-id="1f19f-118">A nova taxa de zoom permanecerá em vigor até que seja restaurada ao tamanho original ou alterada novamente.</span><span class="sxs-lookup"><span data-stu-id="1f19f-118">The new zoom ratio stays in effect until it is restored to the original size or changed again.</span></span> <span data-ttu-id="1f19f-119">Em outras palavras, duas chamadas para esse método especificando um *iZoomRatio* de dois resultarão em uma taxa de zoom quatro vezes maior do que o tamanho original do vídeo.</span><span class="sxs-lookup"><span data-stu-id="1f19f-119">In other words, two calls to this method specifying an *iZoomRatio* of two will result in a zoom ratio four times larger than the original video size.</span></span> <span data-ttu-id="1f19f-120">Se o usuário tentar aplicar zoom além do que o hardware pode dar suporte, esse método terá sucesso, mas não fará nada.</span><span class="sxs-lookup"><span data-stu-id="1f19f-120">If the user tries to zoom beyond what the hardware can support, this method will succeed but do nothing.</span></span>

<span data-ttu-id="1f19f-121">O método [**SetClipVideoRect**](setclipvideorect-method.md) é outra maneira de ampliar; a única diferença entre os dois métodos é a maneira como o retângulo de zoom é especificado.</span><span class="sxs-lookup"><span data-stu-id="1f19f-121">The [**SetClipVideoRect**](setclipvideorect-method.md) method is another way to zoom in; the only difference between the two methods is the way in which the zoom rectangle is specified.</span></span>

 

 



