---
description: Define opções para executar cálculos de distância poliedt, ao ajustar uma textura a uma superfície curva. Use esse sinalizador para escolher entre os cálculos de alta qualidade versus rápidos ao calcular um Atlas de textura.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumeração D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768322"
---
# <a name="d3dxuvatlas-enumeration"></a><span data-ttu-id="6fea3-104">Enumeração D3DXUVATLAS</span><span class="sxs-lookup"><span data-stu-id="6fea3-104">D3DXUVATLAS enumeration</span></span>

<span data-ttu-id="6fea3-105">Define opções para executar cálculos de distância poliedt, ao ajustar uma textura a uma superfície curva.</span><span class="sxs-lookup"><span data-stu-id="6fea3-105">Defines options for performing geodesic distance calculations, when fitting a texture to a curved surface.</span></span> <span data-ttu-id="6fea3-106">Use esse sinalizador para escolher entre os cálculos de alta qualidade versus rápidos ao calcular um Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="6fea3-106">Use this flag to choose between high quality versus fast calculations when computing a texture atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fea3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fea3-107">Syntax</span></span>


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a><span data-ttu-id="6fea3-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6fea3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6fea3-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="6fea3-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="6fea3-110">As malhas com mais de 25K faces terão o método de distância rápida geodasic aplicado a elas, enquanto as malhas com menos de 25K faces terão o método de distância poliedro de qualidade mais alto aplicado a elas em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6fea3-110">Meshes with more than 25k faces will have the fast geodasic distance method applied to them while meshes with fewer than 25k faces will have the higher quality geodesic distance method applied to them instead.</span></span>

</dd> <dt>

<span data-ttu-id="6fea3-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**\_Poliedt D3DXUVATLAS \_ rápido**</span><span class="sxs-lookup"><span data-stu-id="6fea3-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS\_GEODESIC\_FAST**</span></span>
</dt> <dd>

<span data-ttu-id="6fea3-112">Usa aproximações para melhorar a velocidade do gráfico ao custo de ampliação ou mais gráficos de saída para a malha.</span><span class="sxs-lookup"><span data-stu-id="6fea3-112">Uses approximations to improve charting speed at the cost of added stretch or more charts being output for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6fea3-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**\_Qualidade de poliedro D3DXUVATLAS \_**</span><span class="sxs-lookup"><span data-stu-id="6fea3-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS\_GEODESIC\_QUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="6fea3-114">Fornece gráficos de melhor qualidade, mas requer mais tempo e memória do que o rápido.</span><span class="sxs-lookup"><span data-stu-id="6fea3-114">Provides better quality charts, but requires more time and memory than fast.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fea3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fea3-115">Requirements</span></span>



| <span data-ttu-id="6fea3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fea3-116">Requirement</span></span> | <span data-ttu-id="6fea3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6fea3-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fea3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fea3-118">Header</span></span><br/> | <dl> <span data-ttu-id="6fea3-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fea3-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fea3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fea3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fea3-121">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="6fea3-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




