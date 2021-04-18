---
description: Defina os dados de índice da malha.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'Método ID3DX10Mesh:: SetIndexData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788694"
---
# <a name="id3dx10meshsetindexdata-method"></a><span data-ttu-id="cc594-103">Método ID3DX10Mesh:: SetIndexData</span><span class="sxs-lookup"><span data-stu-id="cc594-103">ID3DX10Mesh::SetIndexData method</span></span>

<span data-ttu-id="cc594-104">Defina os dados de índice da malha.</span><span class="sxs-lookup"><span data-stu-id="cc594-104">Set the mesh's index data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc594-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc594-105">Syntax</span></span>


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a><span data-ttu-id="cc594-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc594-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc594-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc594-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc594-108">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="cc594-108">Type: **const void\***</span></span>

<span data-ttu-id="cc594-109">Os dados do índice.</span><span class="sxs-lookup"><span data-stu-id="cc594-109">The index data.</span></span>

</dd> <dt>

<span data-ttu-id="cc594-110">*cIndices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc594-110">*cIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc594-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc594-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc594-112">O número de índices em pData.</span><span class="sxs-lookup"><span data-stu-id="cc594-112">The number of indices in pData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc594-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc594-113">Return value</span></span>

<span data-ttu-id="cc594-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc594-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc594-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cc594-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc594-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc594-116">Requirements</span></span>



| <span data-ttu-id="cc594-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc594-117">Requirement</span></span> | <span data-ttu-id="cc594-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cc594-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc594-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc594-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cc594-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc594-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc594-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc594-121">Library</span></span><br/> | <dl> <span data-ttu-id="cc594-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc594-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc594-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc594-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc594-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="cc594-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="cc594-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cc594-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
