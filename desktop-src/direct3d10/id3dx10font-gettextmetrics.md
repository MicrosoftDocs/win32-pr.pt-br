---
description: Recuperar características de fonte.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'Método ID3DX10Font:: GetTextMetrics (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506489"
---
# <a name="id3dx10fontgettextmetrics-method"></a><span data-ttu-id="79bfb-103">Método ID3DX10Font:: GetTextMetrics</span><span class="sxs-lookup"><span data-stu-id="79bfb-103">ID3DX10Font::GetTextMetrics method</span></span>

<span data-ttu-id="79bfb-104">Recuperar características de fonte.</span><span class="sxs-lookup"><span data-stu-id="79bfb-104">Retrieve font characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="79bfb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79bfb-105">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="79bfb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79bfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79bfb-107">*pTextMetrics* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79bfb-107">*pTextMetrics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79bfb-108">Tipo: **TEXTMETRIC \***</span><span class="sxs-lookup"><span data-stu-id="79bfb-108">Type: **TEXTMETRIC\***</span></span>

<span data-ttu-id="79bfb-109">Ponteiro para uma estrutura [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) , que contém propriedades de fonte.</span><span class="sxs-lookup"><span data-stu-id="79bfb-109">Pointer to a [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) structure, which contains font properties.</span></span> <span data-ttu-id="79bfb-110">Se o Unicode for definido, a função retornará uma estrutura TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="79bfb-110">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="79bfb-111">Caso contrário, a função retorna uma estrutura textmetrica.</span><span class="sxs-lookup"><span data-stu-id="79bfb-111">Otherwise, the function returns a TEXTMETRICA structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79bfb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79bfb-112">Return value</span></span>

<span data-ttu-id="79bfb-113">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79bfb-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79bfb-114">Diferente de zero se a função for bem-sucedida; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="79bfb-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="79bfb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79bfb-115">Requirements</span></span>



| <span data-ttu-id="79bfb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="79bfb-116">Requirement</span></span> | <span data-ttu-id="79bfb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="79bfb-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79bfb-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79bfb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="79bfb-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="79bfb-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="79bfb-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79bfb-120">Library</span></span><br/> | <dl> <span data-ttu-id="79bfb-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79bfb-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79bfb-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="79bfb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79bfb-123">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="79bfb-123">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="79bfb-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="79bfb-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
