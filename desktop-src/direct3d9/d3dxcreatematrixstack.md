---
description: Cria uma instância da interface ID3DXMATRIXStack.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: Função D3DXCreateMatrixStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797545"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a><span data-ttu-id="06c6b-103">Função D3DXCreateMatrixStack (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="06c6b-103">D3DXCreateMatrixStack function (D3dx9math.h)</span></span>

<span data-ttu-id="06c6b-104">Cria uma instância da interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="06c6b-104">Creates an instance of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06c6b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="06c6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06c6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c6b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="06c6b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c6b-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06c6b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06c6b-109">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="06c6b-109">Not implemented.</span></span> <span data-ttu-id="06c6b-110">Especifique zero.</span><span class="sxs-lookup"><span data-stu-id="06c6b-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="06c6b-111">*ppStack* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="06c6b-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06c6b-112">Tipo: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="06c6b-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="06c6b-113">Endereço de um ponteiro preenchido com um ponteiro de interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) se a função tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="06c6b-113">Address of a pointer filled with an [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface pointer if the function succeeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c6b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06c6b-114">Return value</span></span>

<span data-ttu-id="06c6b-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06c6b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06c6b-116">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06c6b-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06c6b-117">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="06c6b-117">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c6b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c6b-118">Requirements</span></span>



| <span data-ttu-id="06c6b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c6b-119">Requirement</span></span> | <span data-ttu-id="06c6b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="06c6b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c6b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06c6b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="06c6b-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c6b-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="06c6b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06c6b-123">Library</span></span><br/> | <dl> <span data-ttu-id="06c6b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06c6b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06c6b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="06c6b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c6b-126">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="06c6b-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
