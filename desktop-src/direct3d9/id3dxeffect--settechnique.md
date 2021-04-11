---
description: Define a técnica ativa.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'Método ID3DXEffect:: settécnica (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e93fbff9eb74e8885675b7ccf4ea69cc53d5da53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930554"
---
# <a name="id3dxeffectsettechnique-method"></a><span data-ttu-id="6d5ad-103">Método ID3DXEffect:: settécnica</span><span class="sxs-lookup"><span data-stu-id="6d5ad-103">ID3DXEffect::SetTechnique method</span></span>

<span data-ttu-id="6d5ad-104">Define a técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="6d5ad-104">Sets the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d5ad-105">Syntax</span></span>


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="6d5ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d5ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d5ad-107">*hTechnique* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d5ad-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5ad-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6d5ad-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6d5ad-109">Identificador exclusivo da técnica.</span><span class="sxs-lookup"><span data-stu-id="6d5ad-109">Unique handle to the technique.</span></span> <span data-ttu-id="6d5ad-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6d5ad-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d5ad-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d5ad-111">Return value</span></span>

<span data-ttu-id="6d5ad-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d5ad-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d5ad-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d5ad-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6d5ad-114">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6d5ad-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d5ad-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d5ad-115">Requirements</span></span>



| <span data-ttu-id="6d5ad-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d5ad-116">Requirement</span></span> | <span data-ttu-id="6d5ad-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6d5ad-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d5ad-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d5ad-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6d5ad-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d5ad-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6d5ad-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d5ad-120">Library</span></span><br/> | <dl> <span data-ttu-id="6d5ad-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d5ad-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6d5ad-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d5ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d5ad-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="6d5ad-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




