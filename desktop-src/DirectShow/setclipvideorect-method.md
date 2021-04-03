---
description: O método SetClipVideoRect amplia a exibição de vídeo para o subretângulo especificado.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Método SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645848"
---
# <a name="setclipvideorect-method"></a><span data-ttu-id="e3a24-103">Método SetClipVideoRect</span><span class="sxs-lookup"><span data-stu-id="e3a24-103">SetClipVideoRect Method</span></span>

> [!Note]  
> <span data-ttu-id="e3a24-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e3a24-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e3a24-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e3a24-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e3a24-106">O `SetClipVideoRect` método amplia a exibição de vídeo para o subretângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="e3a24-106">The `SetClipVideoRect` method zooms the video display to the specified subrectangle.</span></span>

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a><span data-ttu-id="e3a24-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a24-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a24-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span><span class="sxs-lookup"><span data-stu-id="e3a24-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span></span>
</dt> <dd>

<span data-ttu-id="e3a24-109">Especifica um objeto [DVDRect](dvdrect-object.md) , que contém o retângulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="e3a24-109">Specifies a [DVDRect](dvdrect-object.md) object, which contains the clipping rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a24-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e3a24-110">Return Value</span></span>

<span data-ttu-id="e3a24-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e3a24-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a24-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a24-112">Remarks</span></span>

<span data-ttu-id="e3a24-113">Quando você define um novo retângulo de recorte, o objeto amplia essa área para caber nas dimensões de exibição gerais do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3a24-113">When you set a new clipping rectangle, the object enlarges that area to fit within the application's overall display dimensions.</span></span> <span data-ttu-id="e3a24-114">Isso cria o efeito de zoom em uma área específica da tela.</span><span class="sxs-lookup"><span data-stu-id="e3a24-114">This creates the effect zooming in on a particular area of the screen.</span></span> <span data-ttu-id="e3a24-115">Para especificar o retângulo, crie um novo objeto [DVDRect](dvdrect-object.md) e preencha suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e3a24-115">To specify the rectangle, create a new [DVDRect](dvdrect-object.md) object and fill in its properties.</span></span>

<span data-ttu-id="e3a24-116">O retângulo mais comum para exibição de vídeo é 720 x 540.</span><span class="sxs-lookup"><span data-stu-id="e3a24-116">The most common rectangle for video display is 720 x 540.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3a24-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3a24-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a24-118">**GetClipVideoRect**</span><span class="sxs-lookup"><span data-stu-id="e3a24-118">**GetClipVideoRect**</span></span>](getclipvideorect-method.md)
</dt> </dl>

 

 



