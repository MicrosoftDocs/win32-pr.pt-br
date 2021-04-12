---
description: Amplia o padrão Stipple ao longo da direção da linha.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'Método ID3DXLine:: SetPatternScale (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173199"
---
# <a name="id3dxlinesetpatternscale-method"></a><span data-ttu-id="cacd6-103">Método ID3DXLine:: SetPatternScale</span><span class="sxs-lookup"><span data-stu-id="cacd6-103">ID3DXLine::SetPatternScale method</span></span>

<span data-ttu-id="cacd6-104">Amplia o padrão Stipple ao longo da direção da linha.</span><span class="sxs-lookup"><span data-stu-id="cacd6-104">Stretches the stipple pattern along the line direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="cacd6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cacd6-105">Syntax</span></span>


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a><span data-ttu-id="cacd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cacd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cacd6-107">*fPatternScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cacd6-107">*fPatternScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cacd6-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cacd6-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cacd6-109">Valor de dimensionamento do padrão Stipple.</span><span class="sxs-lookup"><span data-stu-id="cacd6-109">Stipple pattern scaling value.</span></span> <span data-ttu-id="cacd6-110">1.0 f é o valor padrão e não representa dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="cacd6-110">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="cacd6-111">Um valor menor que 1,0 f reduz o padrão e um valor maior que 1,0 amplia o padrão.</span><span class="sxs-lookup"><span data-stu-id="cacd6-111">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cacd6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cacd6-112">Return value</span></span>

<span data-ttu-id="cacd6-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cacd6-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cacd6-114">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cacd6-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cacd6-115">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="cacd6-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="cacd6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cacd6-116">Requirements</span></span>



| <span data-ttu-id="cacd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cacd6-117">Requirement</span></span> | <span data-ttu-id="cacd6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cacd6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cacd6-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cacd6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cacd6-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cacd6-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cacd6-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cacd6-121">Library</span></span><br/> | <dl> <span data-ttu-id="cacd6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cacd6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cacd6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cacd6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cacd6-124">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="cacd6-124">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
