---
description: Obtém um status literal de um parâmetro. Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'Método ID3DXEffectCompiler:: getliteral (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760642"
---
# <a name="id3dxeffectcompilergetliteral-method"></a><span data-ttu-id="fca19-104">Método ID3DXEffectCompiler:: getliteral</span><span class="sxs-lookup"><span data-stu-id="fca19-104">ID3DXEffectCompiler::GetLiteral method</span></span>

<span data-ttu-id="fca19-105">Obtém um status literal de um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fca19-105">Gets a literal status of a parameter.</span></span> <span data-ttu-id="fca19-106">Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.</span><span class="sxs-lookup"><span data-stu-id="fca19-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca19-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fca19-107">Syntax</span></span>


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="fca19-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fca19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fca19-109">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fca19-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fca19-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fca19-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fca19-111">Identificador exclusivo para um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fca19-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="fca19-112">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fca19-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fca19-113">*pLiteral* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fca19-113">*pLiteral* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fca19-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fca19-114">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fca19-115">Retornará true se o parâmetro for um literal e false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fca19-115">Returns True if the parameter is a literal, and False otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fca19-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fca19-116">Return value</span></span>

<span data-ttu-id="fca19-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fca19-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fca19-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fca19-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fca19-119">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fca19-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fca19-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fca19-120">Remarks</span></span>

<span data-ttu-id="fca19-121">Esses métodos só alteram se o parâmetro é um literal ou não.</span><span class="sxs-lookup"><span data-stu-id="fca19-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="fca19-122">Para alterar o valor de um parâmetro, use um método como [**ID3DXBaseEffect:: setbool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="fca19-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fca19-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fca19-123">Requirements</span></span>



| <span data-ttu-id="fca19-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca19-124">Requirement</span></span> | <span data-ttu-id="fca19-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fca19-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca19-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fca19-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fca19-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca19-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fca19-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fca19-128">Library</span></span><br/> | <dl> <span data-ttu-id="fca19-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fca19-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fca19-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fca19-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca19-131">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="fca19-131">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="fca19-132">Usos e literais (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fca19-132">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="fca19-133">**ID3DXEffectCompiler:: setliteral**</span><span class="sxs-lookup"><span data-stu-id="fca19-133">**ID3DXEffectCompiler::SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
