---
description: Define os tipos de textura de amostra para sombreadores de vértice.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Enumeração de D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370922"
---
# <a name="d3dsampler_texture_type-enumeration"></a><span data-ttu-id="1e109-103">Enumeração de tipo de \_ textura D3DSAMPLER \_</span><span class="sxs-lookup"><span data-stu-id="1e109-103">D3DSAMPLER\_TEXTURE\_TYPE enumeration</span></span>

<span data-ttu-id="1e109-104">Define os tipos de textura de amostra para sombreadores de vértice.</span><span class="sxs-lookup"><span data-stu-id="1e109-104">Defines the sampler texture types for vertex shaders.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e109-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e109-105">Syntax</span></span>


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1e109-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1e109-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e109-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="1e109-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="1e109-108">Valor não inicializado.</span><span class="sxs-lookup"><span data-stu-id="1e109-108">Uninitialized value.</span></span> <span data-ttu-id="1e109-109">O valor desse elemento é 0 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="1e109-109">The value of this element is 0 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="1e109-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**</span><span class="sxs-lookup"><span data-stu-id="1e109-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT\_2D**</span></span>
</dt> <dd>

<span data-ttu-id="1e109-111">Declarando uma textura 2D.</span><span class="sxs-lookup"><span data-stu-id="1e109-111">Declaring a 2D texture.</span></span> <span data-ttu-id="1e109-112">O valor desse elemento é 2 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="1e109-112">The value of this element is 2 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="1e109-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cubo D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="1e109-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT\_CUBE**</span></span>
</dt> <dd>

<span data-ttu-id="1e109-114">Declarando uma textura de cubo.</span><span class="sxs-lookup"><span data-stu-id="1e109-114">Declaring a cube texture.</span></span> <span data-ttu-id="1e109-115">O valor desse elemento é 3 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="1e109-115">The value of this element is 3 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="1e109-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volume D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="1e109-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="1e109-117">Declarando uma textura de volume.</span><span class="sxs-lookup"><span data-stu-id="1e109-117">Declaring a volume texture.</span></span> <span data-ttu-id="1e109-118">O valor desse elemento é 4 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="1e109-118">The value of this element is 4 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="1e109-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1e109-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1e109-120">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="1e109-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1e109-121">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1e109-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1e109-122">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="1e109-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e109-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e109-123">Requirements</span></span>



| <span data-ttu-id="1e109-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e109-124">Requirement</span></span> | <span data-ttu-id="1e109-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1e109-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e109-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e109-126">Header</span></span><br/> | <dl> <span data-ttu-id="1e109-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e109-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e109-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e109-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e109-129">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="1e109-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




