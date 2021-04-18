---
description: Carregar dados filho de malha de um arquivo. x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'Método ID3DXLoadUserData:: LoadMeshChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768273"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a><span data-ttu-id="0787a-103">Método ID3DXLoadUserData:: LoadMeshChildData</span><span class="sxs-lookup"><span data-stu-id="0787a-103">ID3DXLoadUserData::LoadMeshChildData method</span></span>

<span data-ttu-id="0787a-104">Carregar dados filho de malha de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="0787a-104">Load mesh child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0787a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0787a-105">Syntax</span></span>


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="0787a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0787a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0787a-107">*pMeshContainer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0787a-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0787a-108">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="0787a-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="0787a-109">Ponteiro para um contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="0787a-109">Pointer to a mesh container.</span></span> <span data-ttu-id="0787a-110">Consulte [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0787a-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0787a-111">*pXofChildData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0787a-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0787a-112">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="0787a-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="0787a-113">Ponteiro para uma estrutura de dados de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="0787a-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="0787a-114">Isso é definido em Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="0787a-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0787a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0787a-115">Return value</span></span>

<span data-ttu-id="0787a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0787a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0787a-117">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0787a-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0787a-118">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0787a-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0787a-119">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="0787a-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0787a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0787a-120">Requirements</span></span>



| <span data-ttu-id="0787a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0787a-121">Requirement</span></span> | <span data-ttu-id="0787a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0787a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0787a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0787a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0787a-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0787a-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0787a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0787a-125">Library</span></span><br/> | <dl> <span data-ttu-id="0787a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0787a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0787a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0787a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0787a-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="0787a-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




