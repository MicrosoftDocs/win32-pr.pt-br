---
description: Adicione um objeto de nível superior antes da hierarquia de quadros.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'Método ID3DXSaveUserData:: AddTopLevelDataObjectsPre (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769151"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a><span data-ttu-id="7ea5a-103">Método ID3DXSaveUserData:: AddTopLevelDataObjectsPre</span><span class="sxs-lookup"><span data-stu-id="7ea5a-103">ID3DXSaveUserData::AddTopLevelDataObjectsPre method</span></span>

<span data-ttu-id="7ea5a-104">Adicione um objeto de nível superior antes da hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="7ea5a-104">Add a top level object before the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea5a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ea5a-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="7ea5a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ea5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea5a-107">*pXofSave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ea5a-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea5a-108">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="7ea5a-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="7ea5a-109">Ponteiro para um arquivo. x salvar objeto.</span><span class="sxs-lookup"><span data-stu-id="7ea5a-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="7ea5a-110">Use este ponteiro para chamar [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar o objeto de dados a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="7ea5a-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="7ea5a-111">Em seguida, chame [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) para salvar os dados.</span><span class="sxs-lookup"><span data-stu-id="7ea5a-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ea5a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ea5a-112">Return value</span></span>

<span data-ttu-id="7ea5a-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ea5a-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ea5a-114">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7ea5a-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7ea5a-115">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ea5a-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7ea5a-116">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="7ea5a-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ea5a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ea5a-117">Requirements</span></span>



| <span data-ttu-id="7ea5a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ea5a-118">Requirement</span></span> | <span data-ttu-id="7ea5a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7ea5a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea5a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ea5a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7ea5a-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ea5a-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7ea5a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ea5a-122">Library</span></span><br/> | <dl> <span data-ttu-id="7ea5a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ea5a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ea5a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ea5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea5a-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="7ea5a-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
