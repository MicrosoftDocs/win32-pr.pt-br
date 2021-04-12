---
description: Recupera características de fonte que são identificadas em uma estrutura TEXTMETRIC. Esse método dá suporte às configurações de compilador ANSI e Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'Método ID3DXFont:: GetTextMetrics (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298602"
---
# <a name="id3dxfontgettextmetrics-method"></a><span data-ttu-id="1ade0-104">Método ID3DXFont:: GetTextMetrics</span><span class="sxs-lookup"><span data-stu-id="1ade0-104">ID3DXFont::GetTextMetrics method</span></span>

<span data-ttu-id="1ade0-105">Recupera características de fonte que são identificadas em uma estrutura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="1ade0-105">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="1ade0-106">Esse método dá suporte às configurações de compilador ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ade0-106">This method supports ANSI and Unicode compiler settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ade0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ade0-107">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="1ade0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ade0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ade0-109">*pTextMetrics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ade0-109">*pTextMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ade0-110">Tipo: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span><span class="sxs-lookup"><span data-stu-id="1ade0-110">Type: **[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span></span>

<span data-ttu-id="1ade0-111">Ponteiro para uma estrutura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , que contém propriedades de fonte.</span><span class="sxs-lookup"><span data-stu-id="1ade0-111">Pointer to a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure, which contains font properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ade0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ade0-112">Return value</span></span>

<span data-ttu-id="1ade0-113">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ade0-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ade0-114">Diferente de zero se a função for bem-sucedida; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="1ade0-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ade0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ade0-115">Remarks</span></span>

<span data-ttu-id="1ade0-116">A configuração do compilador também determina o tipo de estrutura.</span><span class="sxs-lookup"><span data-stu-id="1ade0-116">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="1ade0-117">Se o Unicode for definido, a função retornará uma estrutura TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="1ade0-117">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="1ade0-118">Caso contrário, a chamada de função retorna uma estrutura textmetrica.</span><span class="sxs-lookup"><span data-stu-id="1ade0-118">Otherwise, the function call returns a TEXTMETRICA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ade0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ade0-119">Requirements</span></span>



| <span data-ttu-id="1ade0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ade0-120">Requirement</span></span> | <span data-ttu-id="1ade0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1ade0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ade0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ade0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1ade0-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ade0-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1ade0-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ade0-124">Library</span></span><br/> | <dl> <span data-ttu-id="1ade0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ade0-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ade0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ade0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ade0-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="1ade0-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
