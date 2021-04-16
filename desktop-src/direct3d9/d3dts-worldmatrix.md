---
description: Mapeia índices no intervalo de 0 a 255 para os Estados de transformação correspondentes.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Macro D3DTS_WORLDMATRIX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506468"
---
# <a name="d3dts_worldmatrix-macro"></a><span data-ttu-id="8cff7-103">\_Macro D3DTS WORLDMATRIX</span><span class="sxs-lookup"><span data-stu-id="8cff7-103">D3DTS\_WORLDMATRIX macro</span></span>

<span data-ttu-id="8cff7-104">Mapeia índices no intervalo de 0 a 255 para os Estados de transformação correspondentes.</span><span class="sxs-lookup"><span data-stu-id="8cff7-104">Maps indices in the range 0 through 255 to the corresponding transform states.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cff7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cff7-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a><span data-ttu-id="8cff7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cff7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cff7-107">*index*</span><span class="sxs-lookup"><span data-stu-id="8cff7-107">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="8cff7-108">Um valor de índice no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="8cff7-108">An index value in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cff7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cff7-109">Return value</span></span>

<span data-ttu-id="8cff7-110">O [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) que mapeia para o *índice* fornecido.</span><span class="sxs-lookup"><span data-stu-id="8cff7-110">The [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) that maps to the given *index*.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cff7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cff7-111">Remarks</span></span>

<span data-ttu-id="8cff7-112">Os Estados de transformação no intervalo de 256 a 511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8cff7-112">Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cff7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cff7-113">Requirements</span></span>



| <span data-ttu-id="8cff7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cff7-114">Requirement</span></span> | <span data-ttu-id="8cff7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8cff7-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cff7-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cff7-116">Header</span></span><br/> | <dl> <span data-ttu-id="8cff7-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cff7-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cff7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cff7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cff7-119">Macros</span><span class="sxs-lookup"><span data-stu-id="8cff7-119">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="8cff7-120">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="8cff7-120">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
