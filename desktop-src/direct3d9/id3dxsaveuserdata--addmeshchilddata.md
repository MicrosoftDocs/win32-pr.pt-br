---
description: Adicione dados filho à malha.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'Método ID3DXSaveUserData:: AddMeshChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173173"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a><span data-ttu-id="7b5a3-103">Método ID3DXSaveUserData:: AddMeshChildData</span><span class="sxs-lookup"><span data-stu-id="7b5a3-103">ID3DXSaveUserData::AddMeshChildData method</span></span>

<span data-ttu-id="7b5a3-104">Adicione dados filho à malha.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-104">Add child data to the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b5a3-105">Syntax</span></span>


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a><span data-ttu-id="7b5a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b5a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b5a3-107">*pMeshContainer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b5a3-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a3-108">Tipo: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b5a3-108">Type: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="7b5a3-109">Ponteiro para um contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-109">Pointer to a mesh container.</span></span> <span data-ttu-id="7b5a3-110">Consulte [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="7b5a3-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b5a3-111">*pXofSave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b5a3-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a3-112">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="7b5a3-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="7b5a3-113">Ponteiro para um arquivo. x salvar objeto.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="7b5a3-114">Use o ponteiro para chamar [**ID3DXFileSaveObject:: Adddataobject**](id3dxfilesaveobject--adddataobject.md) para adicionar um objeto de dados filho.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="7b5a3-115">Não salve os dados com [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="7b5a3-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b5a3-116">*pXofMeshData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b5a3-116">*pXofMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5a3-117">Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="7b5a3-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="7b5a3-118">Ponteiro para um nó de dados de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="7b5a3-119">Use o ponteiro para chamar [**ID3DXFileSaveData:: Adddataobject**](id3dxfilesavedata--adddataobject.md) para adicionar um objeto de dados filho.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b5a3-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b5a3-120">Return value</span></span>

<span data-ttu-id="7b5a3-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b5a3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b5a3-122">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7b5a3-123">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7b5a3-124">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="7b5a3-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5a3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b5a3-125">Requirements</span></span>



| <span data-ttu-id="7b5a3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b5a3-126">Requirement</span></span> | <span data-ttu-id="7b5a3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7b5a3-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5a3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b5a3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7b5a3-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b5a3-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7b5a3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b5a3-130">Library</span></span><br/> | <dl> <span data-ttu-id="7b5a3-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b5a3-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b5a3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b5a3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5a3-133">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="7b5a3-133">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
