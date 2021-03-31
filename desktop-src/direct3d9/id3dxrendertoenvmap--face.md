---
description: Inicie o desenho de cada face de um mapa de ambiente.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'Método ID3DXRenderToEnvMap:: face (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664104"
---
# <a name="id3dxrendertoenvmapface-method"></a><span data-ttu-id="45381-103">Método ID3DXRenderToEnvMap:: face</span><span class="sxs-lookup"><span data-stu-id="45381-103">ID3DXRenderToEnvMap::Face method</span></span>

<span data-ttu-id="45381-104">Inicie o desenho de cada face de um mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="45381-104">Initiate the drawing of each face of an environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="45381-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45381-105">Syntax</span></span>


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="45381-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45381-107">*Rosto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45381-107">*Face* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45381-108">Tipo: **[ **\_ rostos de D3DCUBEMAP**](./d3dcubemap-faces.md)**</span><span class="sxs-lookup"><span data-stu-id="45381-108">Type: **[**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md)**</span></span>

<span data-ttu-id="45381-109">A primeira face do mapa do cubo ambiental.</span><span class="sxs-lookup"><span data-stu-id="45381-109">The first face of the environmental cube map.</span></span> <span data-ttu-id="45381-110">Consulte [**D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md).</span><span class="sxs-lookup"><span data-stu-id="45381-110">See [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md).</span></span>

</dd> <dt>

<span data-ttu-id="45381-111">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45381-111">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45381-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45381-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45381-113">Uma combinação válida de um ou mais sinalizadores de [ \_ filtro D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="45381-113">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45381-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45381-114">Return value</span></span>

<span data-ttu-id="45381-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45381-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45381-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45381-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="45381-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="45381-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="45381-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="45381-118">Remarks</span></span>

<span data-ttu-id="45381-119">Esse método deve ser chamado uma vez para cada tipo de mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="45381-119">This method must be called once for each type of environment map.</span></span> <span data-ttu-id="45381-120">A única exceção é um mapa de ambiente cúbico que exige que esse método seja chamado seis vezes, uma vez para cada face em rostos D3DCUBEMAPs \_ .</span><span class="sxs-lookup"><span data-stu-id="45381-120">The only exception is a cubic environment map which requires this method to be called six times, once for each face in D3DCUBEMAP\_FACES.</span></span> <span data-ttu-id="45381-121">Para obter mais informações, consulte [mapeamento de ambiente (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="45381-121">For more information, see [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45381-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45381-122">Requirements</span></span>



| <span data-ttu-id="45381-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="45381-123">Requirement</span></span> | <span data-ttu-id="45381-124">Valor</span><span class="sxs-lookup"><span data-stu-id="45381-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45381-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45381-125">Header</span></span><br/>  | <dl> <span data-ttu-id="45381-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="45381-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="45381-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45381-127">Library</span></span><br/> | <dl> <span data-ttu-id="45381-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45381-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45381-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="45381-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45381-130">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="45381-130">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
