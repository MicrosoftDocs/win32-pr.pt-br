---
description: Carregar dados filho do quadro de um arquivo. x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'Método ID3DXLoadUserData:: LoadFrameChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53bde98f0e756fd1baff4c509179f15e8489e74f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506529"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a><span data-ttu-id="fac53-103">Método ID3DXLoadUserData:: LoadFrameChildData</span><span class="sxs-lookup"><span data-stu-id="fac53-103">ID3DXLoadUserData::LoadFrameChildData method</span></span>

<span data-ttu-id="fac53-104">Carregar dados filho do quadro de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="fac53-104">Load frame child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fac53-105">Syntax</span></span>


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="fac53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fac53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac53-107">*pFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fac53-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac53-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="fac53-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="fac53-109">Ponteiro para um contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="fac53-109">Pointer to a mesh container.</span></span> <span data-ttu-id="fac53-110">Consulte [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="fac53-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac53-111">*pXofChildData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fac53-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac53-112">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="fac53-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="fac53-113">Ponteiro para uma estrutura de dados de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="fac53-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="fac53-114">Isso é definido em Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="fac53-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac53-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fac53-115">Return value</span></span>

<span data-ttu-id="fac53-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fac53-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fac53-117">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fac53-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="fac53-118">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fac53-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="fac53-119">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="fac53-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac53-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac53-120">Requirements</span></span>



| <span data-ttu-id="fac53-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac53-121">Requirement</span></span> | <span data-ttu-id="fac53-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fac53-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fac53-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fac53-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fac53-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fac53-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fac53-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fac53-125">Library</span></span><br/> | <dl> <span data-ttu-id="fac53-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fac53-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fac53-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fac53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac53-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="fac53-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




