---
description: Carregar dados de nível superior de um arquivo. x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'Método ID3DXLoadUserData:: LoadTopLevelData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798078"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a><span data-ttu-id="7d8b3-103">Método ID3DXLoadUserData:: LoadTopLevelData</span><span class="sxs-lookup"><span data-stu-id="7d8b3-103">ID3DXLoadUserData::LoadTopLevelData method</span></span>

<span data-ttu-id="7d8b3-104">Carregar dados de nível superior de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="7d8b3-104">Load top level data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d8b3-105">Syntax</span></span>


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="7d8b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d8b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8b3-107">*pXofChildData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d8b3-107">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8b3-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="7d8b3-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="7d8b3-109">Ponteiro para uma estrutura de dados de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="7d8b3-109">Pointer to a .x file data structure.</span></span> <span data-ttu-id="7d8b3-110">Isso é definido em Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="7d8b3-110">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8b3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d8b3-111">Return value</span></span>

<span data-ttu-id="7d8b3-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d8b3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d8b3-113">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7d8b3-113">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7d8b3-114">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7d8b3-114">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7d8b3-115">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="7d8b3-115">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8b3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d8b3-116">Requirements</span></span>



| <span data-ttu-id="7d8b3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d8b3-117">Requirement</span></span> | <span data-ttu-id="7d8b3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7d8b3-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8b3-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d8b3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7d8b3-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d8b3-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7d8b3-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d8b3-121">Library</span></span><br/> | <dl> <span data-ttu-id="7d8b3-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d8b3-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d8b3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d8b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8b3-124">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="7d8b3-124">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




