---
description: Obtém o identificador de uma função.
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: 'Método ID3DXBaseEffect:: GetFunction (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: de0567b605f4a892c1f8274a346a74acfbbc0442
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784589"
---
# <a name="id3dxbaseeffectgetfunction-method"></a><span data-ttu-id="7112a-103">Método ID3DXBaseEffect:: GetFunction</span><span class="sxs-lookup"><span data-stu-id="7112a-103">ID3DXBaseEffect::GetFunction method</span></span>

<span data-ttu-id="7112a-104">Obtém o identificador de uma função.</span><span class="sxs-lookup"><span data-stu-id="7112a-104">Gets the handle of a function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7112a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7112a-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="7112a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7112a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7112a-107">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7112a-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7112a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7112a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7112a-109">Índice de função.</span><span class="sxs-lookup"><span data-stu-id="7112a-109">Function index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7112a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7112a-110">Return value</span></span>

<span data-ttu-id="7112a-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7112a-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7112a-112">Retorna o identificador da função especificada ou **NULL** se o índice era inválido.</span><span class="sxs-lookup"><span data-stu-id="7112a-112">Returns the handle of the specified function, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="7112a-113">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7112a-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7112a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7112a-114">Requirements</span></span>



| <span data-ttu-id="7112a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7112a-115">Requirement</span></span> | <span data-ttu-id="7112a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7112a-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7112a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7112a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7112a-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7112a-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7112a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7112a-119">Library</span></span><br/> | <dl> <span data-ttu-id="7112a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7112a-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7112a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7112a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7112a-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7112a-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
