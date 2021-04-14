---
description: Obtém o valor de escala Stipple-Pattern.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'Método ID3DXLine:: GetPatternScale (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371022"
---
# <a name="id3dxlinegetpatternscale-method"></a><span data-ttu-id="e65f1-103">Método ID3DXLine:: GetPatternScale</span><span class="sxs-lookup"><span data-stu-id="e65f1-103">ID3DXLine::GetPatternScale method</span></span>

<span data-ttu-id="e65f1-104">Obtém o valor de escala Stipple-Pattern.</span><span class="sxs-lookup"><span data-stu-id="e65f1-104">Gets the stipple-pattern scale value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e65f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e65f1-105">Syntax</span></span>


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a><span data-ttu-id="e65f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e65f1-106">Parameters</span></span>

<span data-ttu-id="e65f1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e65f1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e65f1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e65f1-108">Return value</span></span>

<span data-ttu-id="e65f1-109">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e65f1-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e65f1-110">Retorna o valor usado para dimensionar o Stipple-Pattern.</span><span class="sxs-lookup"><span data-stu-id="e65f1-110">Returns the value used to scale the stipple-pattern.</span></span> <span data-ttu-id="e65f1-111">1.0 f é o valor padrão e não representa dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="e65f1-111">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="e65f1-112">Um valor menor que 1,0 f reduz o padrão e um valor maior que 1,0 amplia o padrão.</span><span class="sxs-lookup"><span data-stu-id="e65f1-112">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

## <a name="requirements"></a><span data-ttu-id="e65f1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e65f1-113">Requirements</span></span>



| <span data-ttu-id="e65f1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e65f1-114">Requirement</span></span> | <span data-ttu-id="e65f1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e65f1-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e65f1-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e65f1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e65f1-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e65f1-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e65f1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e65f1-118">Library</span></span><br/> | <dl> <span data-ttu-id="e65f1-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e65f1-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e65f1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e65f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65f1-121">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="e65f1-121">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="e65f1-122">**ID3DXLine::SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="e65f1-122">**ID3DXLine::SetPatternScale**</span></span>](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
