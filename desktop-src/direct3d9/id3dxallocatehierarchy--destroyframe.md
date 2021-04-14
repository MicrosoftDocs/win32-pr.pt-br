---
description: Solicita a desalocação de um objeto de quadro.
ms.assetid: b2793744-1bba-4a2b-938c-44ed316358fd
title: 'ID3DXAllocateHierarchy: método estroyFrame de:D (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4a394501b9967d3f7cb6d3f6b2f30db168438278
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371012"
---
# <a name="id3dxallocatehierarchydestroyframe-method"></a><span data-ttu-id="a7a94-103">ID3DXAllocateHierarchy: método estroyFrame de:D</span><span class="sxs-lookup"><span data-stu-id="a7a94-103">ID3DXAllocateHierarchy::DestroyFrame method</span></span>

<span data-ttu-id="a7a94-104">Solicita a desalocação de um objeto de quadro.</span><span class="sxs-lookup"><span data-stu-id="a7a94-104">Requests deallocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a94-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7a94-105">Syntax</span></span>


```C++
HRESULT DestroyFrame(
  [in] LPD3DXFRAME pFrameToFree
);
```



## <a name="parameters"></a><span data-ttu-id="a7a94-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7a94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7a94-107">*pFrameToFree* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7a94-107">*pFrameToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7a94-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="a7a94-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="a7a94-109">Ponteiro para o quadro a ser desalocado.</span><span class="sxs-lookup"><span data-stu-id="a7a94-109">Pointer to the frame to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7a94-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7a94-110">Return value</span></span>

<span data-ttu-id="a7a94-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7a94-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7a94-112">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a7a94-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="a7a94-113">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7a94-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="a7a94-114">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="a7a94-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7a94-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7a94-115">Requirements</span></span>



| <span data-ttu-id="a7a94-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7a94-116">Requirement</span></span> | <span data-ttu-id="a7a94-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a7a94-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a94-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7a94-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a7a94-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7a94-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a7a94-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7a94-120">Library</span></span><br/> | <dl> <span data-ttu-id="a7a94-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7a94-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a7a94-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7a94-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a94-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="a7a94-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




