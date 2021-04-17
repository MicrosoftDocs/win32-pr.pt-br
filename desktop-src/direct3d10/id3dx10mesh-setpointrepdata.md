---
description: Defina os dados do representante do ponto para a malha.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'Método ID3DX10Mesh:: SetPointRepData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105766450"
---
# <a name="id3dx10meshsetpointrepdata-method"></a><span data-ttu-id="70a26-103">Método ID3DX10Mesh:: SetPointRepData</span><span class="sxs-lookup"><span data-stu-id="70a26-103">ID3DX10Mesh::SetPointRepData method</span></span>

<span data-ttu-id="70a26-104">Defina os dados do representante do ponto para a malha.</span><span class="sxs-lookup"><span data-stu-id="70a26-104">Set the point rep data for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a26-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70a26-105">Syntax</span></span>


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="70a26-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70a26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a26-107">*pPointReps* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70a26-107">*pPointReps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70a26-108">Tipo: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="70a26-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="70a26-109">Os dados do representante do ponto a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="70a26-109">The point rep data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a26-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70a26-110">Return value</span></span>

<span data-ttu-id="70a26-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70a26-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70a26-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="70a26-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70a26-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a26-113">Requirements</span></span>



| <span data-ttu-id="70a26-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a26-114">Requirement</span></span> | <span data-ttu-id="70a26-115">Valor</span><span class="sxs-lookup"><span data-stu-id="70a26-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70a26-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70a26-116">Header</span></span><br/>  | <dl> <span data-ttu-id="70a26-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a26-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="70a26-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70a26-118">Library</span></span><br/> | <dl> <span data-ttu-id="70a26-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70a26-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a26-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="70a26-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a26-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="70a26-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="70a26-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="70a26-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
