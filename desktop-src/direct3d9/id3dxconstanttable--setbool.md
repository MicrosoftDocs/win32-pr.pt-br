---
description: Define um valor booliano.
ms.assetid: 652e5b68-88f3-4b05-959b-38bb530c546a
title: 'Método ID3DXConstantTable:: setbool (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fb38407aeaaf042d8d606c90e075a1891b9557
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664014"
---
# <a name="id3dxconstanttablesetbool-method"></a><span data-ttu-id="5eb53-103">Método ID3DXConstantTable:: setbool</span><span class="sxs-lookup"><span data-stu-id="5eb53-103">ID3DXConstantTable::SetBool method</span></span>

<span data-ttu-id="5eb53-104">Define um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="5eb53-104">Sets a Boolean value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5eb53-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] BOOL              b
);
```



## <a name="parameters"></a><span data-ttu-id="5eb53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5eb53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb53-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5eb53-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb53-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5eb53-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5eb53-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="5eb53-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="5eb53-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5eb53-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb53-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5eb53-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5eb53-112">Identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="5eb53-112">Unique identifier to the constant.</span></span> <span data-ttu-id="5eb53-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5eb53-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5eb53-114">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5eb53-114">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb53-115">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5eb53-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5eb53-116">$True.</span><span class="sxs-lookup"><span data-stu-id="5eb53-116">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb53-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5eb53-117">Return value</span></span>

<span data-ttu-id="5eb53-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5eb53-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5eb53-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5eb53-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5eb53-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5eb53-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb53-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eb53-121">Requirements</span></span>



| <span data-ttu-id="5eb53-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb53-122">Requirement</span></span> | <span data-ttu-id="5eb53-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb53-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb53-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5eb53-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5eb53-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb53-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5eb53-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5eb53-126">Library</span></span><br/> | <dl> <span data-ttu-id="5eb53-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5eb53-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5eb53-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5eb53-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb53-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5eb53-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
