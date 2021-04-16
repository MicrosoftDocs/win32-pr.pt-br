---
title: Ambienteattributes. nineGridMargins
description: O atributo nineGridMargins especifica larguras de margem para o dimensionamento não uniforme do elemento de capa.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- NineGridMargins do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794529"
---
# <a name="ambientattributesninegridmargins"></a><span data-ttu-id="5d343-104">Ambienteattributes. nineGridMargins</span><span class="sxs-lookup"><span data-stu-id="5d343-104">AmbientAttributes.nineGridMargins</span></span>

<span data-ttu-id="5d343-105">O atributo **nineGridMargins** especifica larguras de margem para o dimensionamento não uniforme do elemento de capa.</span><span class="sxs-lookup"><span data-stu-id="5d343-105">The **nineGridMargins** attribute specifies margin widths for non-uniform scaling of the skin element.</span></span>

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a><span data-ttu-id="5d343-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5d343-106">Possible Values</span></span>

<span data-ttu-id="5d343-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém as larguras das margens no formato "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span><span class="sxs-lookup"><span data-stu-id="5d343-107">This attribute is a read/write **String** that contains the widths of the margins in the form "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span></span> <span data-ttu-id="5d343-108">Cada valor de largura é um número que representa a largura, em pixels, de uma margem para a nove grade.</span><span class="sxs-lookup"><span data-stu-id="5d343-108">Each width value is a number representing the width, in pixels, of a margin for the nine grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d343-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d343-109">Remarks</span></span>

<span data-ttu-id="5d343-110">Uma *grade nove* é uma técnica usada para dividir elementos da interface do usuário em nove regiões retangulares organizadas em uma matriz 3 por 3.</span><span class="sxs-lookup"><span data-stu-id="5d343-110">A *nine grid* is a technique used to divide user interface elements into nine rectangular regions arranged in a 3 by 3 matrix.</span></span> <span data-ttu-id="5d343-111">Quando um elemento é redimensionado, as nove regiões de grade podem cada escala por um fator diferente.</span><span class="sxs-lookup"><span data-stu-id="5d343-111">When an element is resized, the nine grid regions can each scale by a different factor.</span></span>

<span data-ttu-id="5d343-112">Cada um dos quatro valores de largura que você especifica representa a largura de uma linha ou coluna de três regiões adjacentes.</span><span class="sxs-lookup"><span data-stu-id="5d343-112">Each of the four width values you specify represents the width of a row or column of three adjacent regions.</span></span> <span data-ttu-id="5d343-113">Cada linha ou coluna formam o lado esquerdo, superior, lado direito ou inferior da grade nove.</span><span class="sxs-lookup"><span data-stu-id="5d343-113">Each row or column forms the left side, top, right side, or bottom of the nine grid.</span></span>

<span data-ttu-id="5d343-114">[Ambienteattributes. resizeImages](ambientattributes-resizeimages.md) deve ser definido como true para que esse atributo funcione.</span><span class="sxs-lookup"><span data-stu-id="5d343-114">[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) must be set to true for this attribute to work.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d343-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d343-115">Requirements</span></span>



| <span data-ttu-id="5d343-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d343-116">Requirement</span></span> | <span data-ttu-id="5d343-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5d343-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="5d343-118">Versão</span><span class="sxs-lookup"><span data-stu-id="5d343-118">Version</span></span><br/> | <span data-ttu-id="5d343-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="5d343-119">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d343-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d343-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d343-121">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="5d343-121">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





