---
description: Aloque espaço para mais Bones.
ms.assetid: f2acd338-f2c2-4340-a673-f36940cf31d9
title: 'Método ID3DX10SkinInfo:: addbones (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4bf9667bd25dd717c4da96c2150e7bd7c45964f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298637"
---
# <a name="id3dx10skininfoaddbones-method"></a><span data-ttu-id="8c2d7-103">Método ID3DX10SkinInfo:: addbones</span><span class="sxs-lookup"><span data-stu-id="8c2d7-103">ID3DX10SkinInfo::AddBones method</span></span>

<span data-ttu-id="8c2d7-104">Aloque espaço para mais Bones.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-104">Allocate space for more bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c2d7-105">Syntax</span></span>


```C++
HRESULT AddBones(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="8c2d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c2d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2d7-107">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="8c2d7-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2d7-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c2d7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c2d7-109">O número de Bones a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-109">The number of bones to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c2d7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c2d7-110">Return value</span></span>

<span data-ttu-id="8c2d7-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c2d7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c2d7-112">Se esse método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8c2d7-113">Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2d7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c2d7-114">Requirements</span></span>



| <span data-ttu-id="8c2d7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c2d7-115">Requirement</span></span> | <span data-ttu-id="8c2d7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8c2d7-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2d7-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c2d7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8c2d7-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c2d7-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c2d7-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c2d7-119">Library</span></span><br/> | <dl> <span data-ttu-id="8c2d7-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c2d7-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2d7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c2d7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2d7-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="8c2d7-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="8c2d7-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8c2d7-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
