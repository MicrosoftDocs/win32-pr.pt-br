---
description: Obtém uma descrição técnica.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'Método ID3DXBaseEffect:: GetTechniqueDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173181"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a><span data-ttu-id="af65e-103">Método ID3DXBaseEffect:: GetTechniqueDesc</span><span class="sxs-lookup"><span data-stu-id="af65e-103">ID3DXBaseEffect::GetTechniqueDesc method</span></span>

<span data-ttu-id="af65e-104">Obtém uma descrição técnica.</span><span class="sxs-lookup"><span data-stu-id="af65e-104">Gets a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="af65e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af65e-105">Syntax</span></span>


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="af65e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af65e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af65e-107">*hTechnique* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af65e-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af65e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="af65e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="af65e-109">Alça de técnica.</span><span class="sxs-lookup"><span data-stu-id="af65e-109">Technique handle.</span></span> <span data-ttu-id="af65e-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="af65e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="af65e-111">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="af65e-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af65e-112">Tipo: **[ **D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="af65e-112">Type: **[**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md)\***</span></span>

<span data-ttu-id="af65e-113">Retorna uma descrição da técnica.</span><span class="sxs-lookup"><span data-stu-id="af65e-113">Returns a description of the technique.</span></span> <span data-ttu-id="af65e-114">Consulte [**D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md).</span><span class="sxs-lookup"><span data-stu-id="af65e-114">See [**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af65e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af65e-115">Return value</span></span>

<span data-ttu-id="af65e-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af65e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af65e-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af65e-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="af65e-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="af65e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="af65e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af65e-119">Requirements</span></span>



| <span data-ttu-id="af65e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="af65e-120">Requirement</span></span> | <span data-ttu-id="af65e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="af65e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af65e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af65e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="af65e-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="af65e-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="af65e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af65e-124">Library</span></span><br/> | <dl> <span data-ttu-id="af65e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af65e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="af65e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="af65e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af65e-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="af65e-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




