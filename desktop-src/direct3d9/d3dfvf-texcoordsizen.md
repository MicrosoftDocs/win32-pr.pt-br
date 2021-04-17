---
description: Constrói padrões de bits que são usados para identificar formatos de coordenadas de textura em uma descrição de FVF. Os resultados dessas macros podem ser combinados em uma descrição de FVF usando o operador OR.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797934"
---
# <a name="d3dfvf_texcoordsizen"></a><span data-ttu-id="63a0f-104">D3DFVF \_ TEXCOORDSIZEN</span><span class="sxs-lookup"><span data-stu-id="63a0f-104">D3DFVF\_TEXCOORDSIZEN</span></span>

<span data-ttu-id="63a0f-105">Constrói padrões de bits que são usados para identificar formatos de coordenadas de textura em uma descrição de FVF.</span><span class="sxs-lookup"><span data-stu-id="63a0f-105">Constructs bit patterns that are used to identify texture coordinate formats within a FVF description.</span></span> <span data-ttu-id="63a0f-106">Os resultados dessas macros podem ser combinados em uma descrição de FVF usando o operador OR.</span><span class="sxs-lookup"><span data-stu-id="63a0f-106">The results of these macros can be combined within a FVF description by using the OR operator.</span></span>

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a><span data-ttu-id="63a0f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63a0f-107">Parameters</span></span>



| <span data-ttu-id="63a0f-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="63a0f-108">Parameter</span></span>                                                                                                    | <span data-ttu-id="63a0f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="63a0f-109">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a0f-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span><span class="sxs-lookup"><span data-stu-id="63a0f-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span></span><br/> | <span data-ttu-id="63a0f-111">Valor que identifica o conjunto de coordenadas de textura no qual o tamanho da coordenada de textura (1-, 2-, 3 ou 4Dimensional) se aplica.</span><span class="sxs-lookup"><span data-stu-id="63a0f-111">Value that identifies the texture coordinate set at which the texture coordinate size (1-, 2-, 3-, or 4Dimensional) applies.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="63a0f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="63a0f-112">Remarks</span></span>

<span data-ttu-id="63a0f-113">As macros **D3DFVF \_ TEXCOORDSIZEN** usam as constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="63a0f-113">The **D3DFVF\_TEXCOORDSIZEN** macros use the following constants.</span></span>


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



<span data-ttu-id="63a0f-114">A seguinte descrição de FVF identifica um formato de vértice que tem uma posição; um normal; cores difusas e especulares; e dois conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="63a0f-114">The following FVF description identifies a vertex format that has a position; a normal; diffuse and specular colors; and two sets of texture coordinates.</span></span> <span data-ttu-id="63a0f-115">O primeiro conjunto de coordenadas de textura inclui um único elemento e o segundo conjunto inclui dois elementos:</span><span class="sxs-lookup"><span data-stu-id="63a0f-115">The first set of texture coordinates includes a single element, and the second set includes two elements:</span></span>


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a><span data-ttu-id="63a0f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63a0f-116">Requirements</span></span>



| <span data-ttu-id="63a0f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a0f-117">Requirement</span></span> | <span data-ttu-id="63a0f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="63a0f-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63a0f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63a0f-119">Header</span></span><br/> | <dl> <span data-ttu-id="63a0f-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="63a0f-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a0f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="63a0f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a0f-122">Macros</span><span class="sxs-lookup"><span data-stu-id="63a0f-122">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="63a0f-123">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="63a0f-123">D3DFVF</span></span>](d3dfvf.md)
</dt> </dl>

 

 




