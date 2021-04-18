---
description: Descreve a resolução da sombra z-buffer que será usada na simulação de iluminação direta do PRT (transferência de radiante de computação) na GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Enumeração D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780701"
---
# <a name="d3dxshgpusimopt-enumeration"></a><span data-ttu-id="ed68b-103">Enumeração D3DXSHGPUSIMOPT</span><span class="sxs-lookup"><span data-stu-id="ed68b-103">D3DXSHGPUSIMOPT enumeration</span></span>

<span data-ttu-id="ed68b-104">Descreve a resolução da sombra z-buffer que será usada na simulação de iluminação direta do PRT (transferência de radiante de computação) na GPU.</span><span class="sxs-lookup"><span data-stu-id="ed68b-104">Describes the resolution of the shadow z-buffer that will be used in Precomputed Radiance Transfer (PRT) direct lighting simulation on the GPU.</span></span> <span data-ttu-id="ed68b-105">Um buffer z de qualidade superior também pode ser especificado para reduzir o ruído nos resultados da simulação de iluminação direta, embora a simulação seja mais lenta.</span><span class="sxs-lookup"><span data-stu-id="ed68b-105">A higher quality z-buffer can also be specified to reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed68b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed68b-106">Syntax</span></span>


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a><span data-ttu-id="ed68b-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="ed68b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed68b-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**</span><span class="sxs-lookup"><span data-stu-id="ed68b-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT\_SHADOWRES256**</span></span>
</dt> <dd>

<span data-ttu-id="ed68b-109">Simulação de baixa resolução.</span><span class="sxs-lookup"><span data-stu-id="ed68b-109">Low resolution simulation.</span></span> <span data-ttu-id="ed68b-110">Uma textura de 256 x 256 pixels é usada na simulação para codificar a sombra z-buffer.</span><span class="sxs-lookup"><span data-stu-id="ed68b-110">A 256 x 256 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ed68b-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**</span><span class="sxs-lookup"><span data-stu-id="ed68b-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT\_SHADOWRES512**</span></span>
</dt> <dd>

<span data-ttu-id="ed68b-112">Simulação de resolução média.</span><span class="sxs-lookup"><span data-stu-id="ed68b-112">Medium resolution simulation.</span></span> <span data-ttu-id="ed68b-113">Uma textura de 512 x 512 pixels é usada na simulação para codificar a sombra z-buffer.</span><span class="sxs-lookup"><span data-stu-id="ed68b-113">A 512 x 512 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span> <span data-ttu-id="ed68b-114">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="ed68b-114">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="ed68b-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**</span><span class="sxs-lookup"><span data-stu-id="ed68b-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT\_SHADOWRES1024**</span></span>
</dt> <dd>

<span data-ttu-id="ed68b-116">Simulação de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="ed68b-116">High resolution simulation.</span></span> <span data-ttu-id="ed68b-117">Uma textura de 1024 x 1024 pixels é usada na simulação para codificar a sombra z-buffer.</span><span class="sxs-lookup"><span data-stu-id="ed68b-117">A 1024 x 1024 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ed68b-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**</span><span class="sxs-lookup"><span data-stu-id="ed68b-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT\_SHADOWRES2048**</span></span>
</dt> <dd>

<span data-ttu-id="ed68b-119">Simulação de resolução mais alta.</span><span class="sxs-lookup"><span data-stu-id="ed68b-119">Highest resolution simulation.</span></span> <span data-ttu-id="ed68b-120">Uma textura de 2048 x 2048 pixels é usada na simulação para codificar a sombra z-buffer.</span><span class="sxs-lookup"><span data-stu-id="ed68b-120">A 2048 x 2048 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ed68b-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ Highquality**</span><span class="sxs-lookup"><span data-stu-id="ed68b-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT\_HIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="ed68b-122">A simulação é de alta precisão, independentemente da resolução selecionada.</span><span class="sxs-lookup"><span data-stu-id="ed68b-122">The simulation is of high precision, regardless of the selected resolution.</span></span> <span data-ttu-id="ed68b-123">Definir esse valor reduzirá o ruído nos resultados da simulação de iluminação direta, embora a simulação seja mais lenta.</span><span class="sxs-lookup"><span data-stu-id="ed68b-123">Setting this value will reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span> <span data-ttu-id="ed68b-124">Pode ser combinado com um dos valores de resolução.</span><span class="sxs-lookup"><span data-stu-id="ed68b-124">May be combined with one of the resolution values.</span></span>

</dd> <dt>

<span data-ttu-id="ed68b-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ed68b-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ed68b-126">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="ed68b-126">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ed68b-127">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ed68b-127">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ed68b-128">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="ed68b-128">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed68b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed68b-129">Remarks</span></span>

<span data-ttu-id="ed68b-130">Somente um dos valores de resolução pode ser especificado e pode ser combinado com o valor de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="ed68b-130">Only one of the resolution values may be specified, and may be combined with the high-quality value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed68b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed68b-131">Requirements</span></span>



| <span data-ttu-id="ed68b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed68b-132">Requirement</span></span> | <span data-ttu-id="ed68b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ed68b-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed68b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed68b-134">Header</span></span><br/> | <dl> <span data-ttu-id="ed68b-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed68b-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed68b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed68b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed68b-137">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="ed68b-137">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




