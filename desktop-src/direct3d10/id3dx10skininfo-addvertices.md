---
description: Aloque espaço para vértices adicionais.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'Método ID3DX10SkinInfo:: addvértices (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750185"
---
# <a name="id3dx10skininfoaddvertices-method"></a><span data-ttu-id="fb06b-103">Método ID3DX10SkinInfo:: addvértices</span><span class="sxs-lookup"><span data-stu-id="fb06b-103">ID3DX10SkinInfo::AddVertices method</span></span>

<span data-ttu-id="fb06b-104">Aloque espaço para vértices adicionais.</span><span class="sxs-lookup"><span data-stu-id="fb06b-104">Allocate space for additional vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb06b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb06b-105">Syntax</span></span>


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="fb06b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb06b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb06b-107">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="fb06b-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb06b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb06b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb06b-109">O número de vértices a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="fb06b-109">The number of vertices to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb06b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb06b-110">Return value</span></span>

<span data-ttu-id="fb06b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb06b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb06b-112">Se esse método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb06b-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fb06b-113">Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fb06b-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb06b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb06b-114">Requirements</span></span>



| <span data-ttu-id="fb06b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb06b-115">Requirement</span></span> | <span data-ttu-id="fb06b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fb06b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb06b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb06b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fb06b-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb06b-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb06b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb06b-119">Library</span></span><br/> | <dl> <span data-ttu-id="fb06b-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb06b-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb06b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb06b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb06b-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="fb06b-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="fb06b-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="fb06b-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
