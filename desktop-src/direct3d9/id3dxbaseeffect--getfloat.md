---
description: Obtém um valor de ponto flutuante.
ms.assetid: 239dd29c-092a-4b9f-ba24-eb6181e91461
title: 'Método ID3DXBaseEffect:: GetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 51edaa1872223727abdc396766552720cd34d726
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763512"
---
# <a name="id3dxbaseeffectgetfloat-method"></a><span data-ttu-id="f9d8e-103">Método ID3DXBaseEffect:: getFloat</span><span class="sxs-lookup"><span data-stu-id="f9d8e-103">ID3DXBaseEffect::GetFloat method</span></span>

<span data-ttu-id="f9d8e-104">Obtém um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f9d8e-104">Gets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d8e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9d8e-105">Syntax</span></span>


```C++
HRESULT GetFloat(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf
);
```



## <a name="parameters"></a><span data-ttu-id="f9d8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9d8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9d8e-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9d8e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d8e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f9d8e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f9d8e-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f9d8e-109">Unique identifier.</span></span> <span data-ttu-id="f9d8e-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f9d8e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9d8e-111">*PF* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9d8e-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d8e-112">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9d8e-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f9d8e-113">Retorna um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f9d8e-113">Returns a floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9d8e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9d8e-114">Return value</span></span>

<span data-ttu-id="f9d8e-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9d8e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9d8e-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9d8e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f9d8e-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f9d8e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d8e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9d8e-118">Requirements</span></span>



| <span data-ttu-id="f9d8e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9d8e-119">Requirement</span></span> | <span data-ttu-id="f9d8e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f9d8e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d8e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9d8e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f9d8e-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d8e-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f9d8e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9d8e-123">Library</span></span><br/> | <dl> <span data-ttu-id="f9d8e-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9d8e-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f9d8e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9d8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d8e-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f9d8e-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f9d8e-127">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="f9d8e-127">**SetFloat**</span></span>](id3dxbaseeffect--setfloat.md)
</dt> </dl>

 

 
