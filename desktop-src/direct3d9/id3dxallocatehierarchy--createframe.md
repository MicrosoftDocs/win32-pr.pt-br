---
description: Solicita a alocação de um objeto de quadro.
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: 'Método ID3DXAllocateHierarchy:: CreateFrame (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6a3a13dd4d3b3dfaffb26632ff6ad5cc8666f86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763272"
---
# <a name="id3dxallocatehierarchycreateframe-method"></a><span data-ttu-id="3b01a-103">Método ID3DXAllocateHierarchy:: CreateFrame</span><span class="sxs-lookup"><span data-stu-id="3b01a-103">ID3DXAllocateHierarchy::CreateFrame method</span></span>

<span data-ttu-id="3b01a-104">Solicita a alocação de um objeto de quadro.</span><span class="sxs-lookup"><span data-stu-id="3b01a-104">Requests allocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b01a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b01a-105">Syntax</span></span>


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## <a name="parameters"></a><span data-ttu-id="3b01a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b01a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b01a-107">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3b01a-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b01a-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b01a-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b01a-109">Nome do quadro a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3b01a-109">Name of the frame to be created.</span></span>

</dd> <dt>

<span data-ttu-id="3b01a-110">*ppNewFrame* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3b01a-110">*ppNewFrame* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3b01a-111">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b01a-111">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="3b01a-112">Retorna o objeto frame criado.</span><span class="sxs-lookup"><span data-stu-id="3b01a-112">Returns the created frame object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b01a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b01a-113">Return value</span></span>

<span data-ttu-id="3b01a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b01a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b01a-115">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3b01a-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="3b01a-116">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3b01a-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="3b01a-117">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="3b01a-117">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b01a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b01a-118">Requirements</span></span>



| <span data-ttu-id="3b01a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b01a-119">Requirement</span></span> | <span data-ttu-id="3b01a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3b01a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b01a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b01a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3b01a-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b01a-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3b01a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b01a-123">Library</span></span><br/> | <dl> <span data-ttu-id="3b01a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b01a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3b01a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b01a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b01a-126">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="3b01a-126">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
