---
description: Adicione dados filho ao quadro.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'Método ID3DXSaveUserData:: AddFrameChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173174"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a><span data-ttu-id="33c0b-103">Método ID3DXSaveUserData:: AddFrameChildData</span><span class="sxs-lookup"><span data-stu-id="33c0b-103">ID3DXSaveUserData::AddFrameChildData method</span></span>

<span data-ttu-id="33c0b-104">Adicione dados filho ao quadro.</span><span class="sxs-lookup"><span data-stu-id="33c0b-104">Add child data to the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c0b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33c0b-105">Syntax</span></span>


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="33c0b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33c0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c0b-107">*pFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c0b-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c0b-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="33c0b-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="33c0b-109">Ponteiro para um contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="33c0b-109">Pointer to a mesh container.</span></span> <span data-ttu-id="33c0b-110">Consulte [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="33c0b-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="33c0b-111">*pXofSave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c0b-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c0b-112">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="33c0b-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="33c0b-113">Ponteiro para um arquivo. x salvar objeto.</span><span class="sxs-lookup"><span data-stu-id="33c0b-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="33c0b-114">Use o ponteiro para chamar [**ID3DXFileSaveObject:: Adddataobject**](id3dxfilesaveobject--adddataobject.md) para adicionar um objeto de dados filho.</span><span class="sxs-lookup"><span data-stu-id="33c0b-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="33c0b-115">Não salve os dados com [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="33c0b-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="33c0b-116">*pXofFrameData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c0b-116">*pXofFrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c0b-117">Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="33c0b-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="33c0b-118">Ponteiro para um nó de dados de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="33c0b-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="33c0b-119">Use o ponteiro para chamar [**ID3DXFileSaveData:: Adddataobject**](id3dxfilesavedata--adddataobject.md) para adicionar um objeto de dados filho.</span><span class="sxs-lookup"><span data-stu-id="33c0b-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c0b-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33c0b-120">Return value</span></span>

<span data-ttu-id="33c0b-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33c0b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33c0b-122">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="33c0b-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="33c0b-123">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33c0b-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="33c0b-124">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="33c0b-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c0b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="33c0b-125">Remarks</span></span>

<span data-ttu-id="33c0b-126">[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) e [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fornecem um mecanismo para adicionar um modelo a um arquivo. x para salvar dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="33c0b-126">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c0b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c0b-127">Requirements</span></span>



| <span data-ttu-id="33c0b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c0b-128">Requirement</span></span> | <span data-ttu-id="33c0b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="33c0b-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33c0b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33c0b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="33c0b-131"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c0b-131"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="33c0b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33c0b-132">Library</span></span><br/> | <dl> <span data-ttu-id="33c0b-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33c0b-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33c0b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="33c0b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c0b-135">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="33c0b-135">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
