---
description: Defina os dados de adjacência da malha.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'Método ID3DX10Mesh:: SetAdjacencyData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6fabced002caf424fa1fcbcefcb3b326b0c71f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793626"
---
# <a name="id3dx10meshsetadjacencydata-method"></a><span data-ttu-id="fcc14-103">Método ID3DX10Mesh:: SetAdjacencyData</span><span class="sxs-lookup"><span data-stu-id="fcc14-103">ID3DX10Mesh::SetAdjacencyData method</span></span>

<span data-ttu-id="fcc14-104">Defina os dados de adjacência da malha.</span><span class="sxs-lookup"><span data-stu-id="fcc14-104">Set the mesh's adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc14-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcc14-105">Syntax</span></span>


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="fcc14-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcc14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc14-107">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc14-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc14-108">Tipo: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcc14-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fcc14-109">Os dados de adjacência a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="fcc14-109">The adjacency data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc14-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcc14-110">Return value</span></span>

<span data-ttu-id="fcc14-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcc14-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcc14-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fcc14-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc14-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc14-113">Requirements</span></span>



| <span data-ttu-id="fcc14-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc14-114">Requirement</span></span> | <span data-ttu-id="fcc14-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fcc14-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc14-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcc14-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fcc14-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc14-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcc14-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcc14-118">Library</span></span><br/> | <dl> <span data-ttu-id="fcc14-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcc14-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc14-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcc14-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc14-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="fcc14-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="fcc14-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="fcc14-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
