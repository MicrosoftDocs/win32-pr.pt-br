---
description: 'Método ID3DXConstantTable:: setvector – define um vetor 4D.'
ms.assetid: d5849a8b-b372-4ad0-8773-8c9c4bac3799
title: 'Método ID3DXConstantTable:: setvector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d7c464cebb050b9fd54c27656505e6f2221fe4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115014"
---
# <a name="id3dxconstanttablesetvector-method"></a><span data-ttu-id="d5e76-103">Método ID3DXConstantTable:: setvector</span><span class="sxs-lookup"><span data-stu-id="d5e76-103">ID3DXConstantTable::SetVector method</span></span>

<span data-ttu-id="d5e76-104">Define um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="d5e76-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e76-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5e76-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="d5e76-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5e76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e76-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5e76-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e76-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d5e76-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d5e76-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="d5e76-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d5e76-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5e76-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e76-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d5e76-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d5e76-112">Identificador exclusivo para a constante de vetor.</span><span class="sxs-lookup"><span data-stu-id="d5e76-112">Unique identifier to the vector constant.</span></span> <span data-ttu-id="d5e76-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d5e76-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5e76-114">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5e76-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e76-115">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5e76-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d5e76-116">Ponteiro para um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="d5e76-116">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e76-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d5e76-117">Return value</span></span>

<span data-ttu-id="d5e76-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5e76-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5e76-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5e76-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5e76-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d5e76-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e76-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e76-121">Requirements</span></span>



| <span data-ttu-id="d5e76-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e76-122">Requirement</span></span> | <span data-ttu-id="d5e76-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d5e76-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e76-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5e76-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5e76-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e76-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d5e76-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5e76-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5e76-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5e76-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d5e76-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d5e76-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e76-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d5e76-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
