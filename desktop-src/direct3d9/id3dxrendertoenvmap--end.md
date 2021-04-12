---
description: Restaurar todos os destinos de renderização e, se necessário, compor todas as faces renderizadas na superfície do mapa do ambiente.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'Método ID3DXRenderToEnvMap:: End (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298562"
---
# <a name="id3dxrendertoenvmapend-method"></a><span data-ttu-id="95e5e-103">Método ID3DXRenderToEnvMap:: End</span><span class="sxs-lookup"><span data-stu-id="95e5e-103">ID3DXRenderToEnvMap::End method</span></span>

<span data-ttu-id="95e5e-104">Restaurar todos os destinos de renderização e, se necessário, compor todas as faces renderizadas na superfície do mapa do ambiente.</span><span class="sxs-lookup"><span data-stu-id="95e5e-104">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e5e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95e5e-105">Syntax</span></span>


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="95e5e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95e5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e5e-107">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95e5e-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e5e-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e5e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e5e-109">Uma combinação válida de um ou mais sinalizadores de [ \_ filtro D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5e-109">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e5e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95e5e-110">Return value</span></span>

<span data-ttu-id="95e5e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95e5e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95e5e-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95e5e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95e5e-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="95e5e-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e5e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95e5e-114">Requirements</span></span>



| <span data-ttu-id="95e5e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="95e5e-115">Requirement</span></span> | <span data-ttu-id="95e5e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="95e5e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95e5e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95e5e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="95e5e-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="95e5e-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="95e5e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95e5e-119">Library</span></span><br/> | <dl> <span data-ttu-id="95e5e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95e5e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95e5e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="95e5e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e5e-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="95e5e-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="95e5e-123">**ID3DXRenderToEnvMap:: face**</span><span class="sxs-lookup"><span data-stu-id="95e5e-123">**ID3DXRenderToEnvMap::Face**</span></span>](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
