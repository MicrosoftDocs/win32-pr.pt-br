---
description: Desmonte um efeito.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: Função D3DXDisassembleEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793322"
---
# <a name="d3dxdisassembleeffect-function"></a><span data-ttu-id="313c8-103">Função D3DXDisassembleEffect</span><span class="sxs-lookup"><span data-stu-id="313c8-103">D3DXDisassembleEffect function</span></span>

<span data-ttu-id="313c8-104">Desmonte um efeito.</span><span class="sxs-lookup"><span data-stu-id="313c8-104">Disassemble an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="313c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="313c8-105">Syntax</span></span>


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="313c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="313c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313c8-107">*pEffect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="313c8-107">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="313c8-108">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="313c8-108">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)**</span></span>

<span data-ttu-id="313c8-109">Ponteiro para uma interface [**ID3DXEffect**](id3dxeffect.md) que contém o efeito.</span><span class="sxs-lookup"><span data-stu-id="313c8-109">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface that contains the effect.</span></span>

</dd> <dt>

<span data-ttu-id="313c8-110">*EnableColorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="313c8-110">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="313c8-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="313c8-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="313c8-112">Habilite a codificação de cores para facilitar a leitura da desmontagem.</span><span class="sxs-lookup"><span data-stu-id="313c8-112">Enable color coding to make the disassembly easier to read.</span></span>

</dd> <dt>

<span data-ttu-id="313c8-113">*ppDisassembly* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="313c8-113">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="313c8-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="313c8-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="313c8-115">Retorna um buffer que contém o sombreador desmontado.</span><span class="sxs-lookup"><span data-stu-id="313c8-115">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="313c8-116">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="313c8-116">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313c8-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="313c8-117">Return value</span></span>

<span data-ttu-id="313c8-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="313c8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="313c8-119">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="313c8-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="313c8-120">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="313c8-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="313c8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="313c8-121">Requirements</span></span>



| <span data-ttu-id="313c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="313c8-122">Requirement</span></span> | <span data-ttu-id="313c8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="313c8-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="313c8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="313c8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="313c8-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="313c8-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="313c8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="313c8-126">Library</span></span><br/> | <dl> <span data-ttu-id="313c8-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="313c8-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="313c8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="313c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313c8-129">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="313c8-129">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
