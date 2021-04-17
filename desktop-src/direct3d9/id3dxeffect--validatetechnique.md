---
description: Valide uma técnica.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'Método ID3DXEffect:: ValidateTechnique (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762387"
---
# <a name="id3dxeffectvalidatetechnique-method"></a><span data-ttu-id="c57c0-103">Método ID3DXEffect:: ValidateTechnique</span><span class="sxs-lookup"><span data-stu-id="c57c0-103">ID3DXEffect::ValidateTechnique method</span></span>

<span data-ttu-id="c57c0-104">Valide uma técnica.</span><span class="sxs-lookup"><span data-stu-id="c57c0-104">Validate a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57c0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c57c0-105">Syntax</span></span>


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="c57c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c57c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c57c0-107">*hTechnique* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c57c0-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c57c0-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c57c0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c57c0-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c57c0-109">Unique identifier.</span></span> <span data-ttu-id="c57c0-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c57c0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c57c0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c57c0-111">Return value</span></span>

<span data-ttu-id="c57c0-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c57c0-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c57c0-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c57c0-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c57c0-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ CONFLICTINGRENDERSTATE, D3DERR \_ CONFLICTINGTEXTUREFILTER, D3DERR \_ DEVICELOST, D3DERR \_ DRIVERINTERNALERROR, D3DERR \_ TOOMANYOPERATIONS, D3DERR \_ UNSUPPORTEDALPHAARG, D3DERR \_ UNSUPPORTEDALPHAOPERATION, D3DERR \_ UNSUPPORTEDCOLORARG, D3DERR \_ UNSUPPORTEDCOLOROPERATION, D3DERR \_ UNSUPPORTEDFACTORVALUE, D3DERR \_ UNSUPPORTEDTEXTUREFILTER e D3DERR \_ WRONGTEXTUREFORMAT.</span><span class="sxs-lookup"><span data-stu-id="c57c0-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_CONFLICTINGRENDERSTATE, D3DERR\_CONFLICTINGTEXTUREFILTER, D3DERR\_DEVICELOST, D3DERR\_DRIVERINTERNALERROR, D3DERR\_TOOMANYOPERATIONS, D3DERR\_UNSUPPORTEDALPHAARG, D3DERR\_UNSUPPORTEDALPHAOPERATION, D3DERR\_UNSUPPORTEDCOLORARG, D3DERR\_UNSUPPORTEDCOLOROPERATION, D3DERR\_UNSUPPORTEDFACTORVALUE, D3DERR\_UNSUPPORTEDTEXTUREFILTER, and D3DERR\_WRONGTEXTUREFORMAT.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57c0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c57c0-115">Requirements</span></span>



| <span data-ttu-id="c57c0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c57c0-116">Requirement</span></span> | <span data-ttu-id="c57c0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c57c0-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57c0-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c57c0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c57c0-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c57c0-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c57c0-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c57c0-120">Library</span></span><br/> | <dl> <span data-ttu-id="c57c0-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c57c0-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c57c0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c57c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57c0-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="c57c0-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="c57c0-124">**ID3DXEffect:: settécnica**</span><span class="sxs-lookup"><span data-stu-id="c57c0-124">**ID3DXEffect::SetTechnique**</span></span>](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




