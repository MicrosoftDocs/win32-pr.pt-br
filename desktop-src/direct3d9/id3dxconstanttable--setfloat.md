---
description: Define um número de ponto flutuante.
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: 'Método ID3DXConstantTable:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5048f08acc470e5244de80f4e5618c7416bc1bbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781542"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="e9bd7-103">Método ID3DXConstantTable:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="e9bd7-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="e9bd7-104">Define um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="e9bd7-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9bd7-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="e9bd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9bd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9bd7-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9bd7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bd7-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e9bd7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e9bd7-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="e9bd7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e9bd7-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9bd7-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bd7-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e9bd7-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e9bd7-112">Identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="e9bd7-112">Unique identifier to the constant.</span></span> <span data-ttu-id="e9bd7-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e9bd7-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9bd7-114">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e9bd7-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bd7-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9bd7-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9bd7-116">Número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="e9bd7-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9bd7-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9bd7-117">Return value</span></span>

<span data-ttu-id="e9bd7-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9bd7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9bd7-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9bd7-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9bd7-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e9bd7-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bd7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9bd7-121">Requirements</span></span>



| <span data-ttu-id="e9bd7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9bd7-122">Requirement</span></span> | <span data-ttu-id="e9bd7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e9bd7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bd7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9bd7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e9bd7-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9bd7-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e9bd7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9bd7-126">Library</span></span><br/> | <dl> <span data-ttu-id="e9bd7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9bd7-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e9bd7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9bd7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bd7-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e9bd7-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
