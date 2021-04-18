---
description: Criar uma pilha de matriz.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: Função D3DXCreateMatrixStack (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370993"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a><span data-ttu-id="77f92-103">Função D3DXCreateMatrixStack (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="77f92-103">D3DXCreateMatrixStack function (D3DX10Math.h)</span></span>

<span data-ttu-id="77f92-104">Criar uma pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="77f92-104">Create a matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77f92-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="77f92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f92-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="77f92-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77f92-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77f92-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77f92-109">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="77f92-109">Not implemented.</span></span> <span data-ttu-id="77f92-110">Especifique zero.</span><span class="sxs-lookup"><span data-stu-id="77f92-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="77f92-111">*ppStack* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="77f92-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f92-112">Tipo: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="77f92-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="77f92-113">O endereço de um ponteiro para uma pilha de matriz (consulte a [**interface ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).</span><span class="sxs-lookup"><span data-stu-id="77f92-113">The address of a pointer to a matrix stack (see [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77f92-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77f92-114">Return value</span></span>

<span data-ttu-id="77f92-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77f92-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77f92-116">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="77f92-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77f92-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77f92-117">Requirements</span></span>



| <span data-ttu-id="77f92-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f92-118">Requirement</span></span> | <span data-ttu-id="77f92-119">Valor</span><span class="sxs-lookup"><span data-stu-id="77f92-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77f92-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77f92-120">Header</span></span><br/>  | <dl> <span data-ttu-id="77f92-121"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="77f92-121"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="77f92-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77f92-122">Library</span></span><br/> | <dl> <span data-ttu-id="77f92-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77f92-123"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="77f92-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="77f92-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f92-125">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="77f92-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
