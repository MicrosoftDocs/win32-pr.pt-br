---
description: Um retorno de chamada para o usuário salvar um modelo de arquivo. x.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'Método ID3DXSaveUserData:: SaveTemplates (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92040629b1b21cbfa1219eee237e357aa056b473
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930742"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a><span data-ttu-id="954ba-103">Método ID3DXSaveUserData:: SaveTemplates</span><span class="sxs-lookup"><span data-stu-id="954ba-103">ID3DXSaveUserData::SaveTemplates method</span></span>

<span data-ttu-id="954ba-104">Um retorno de chamada para o usuário salvar um modelo de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="954ba-104">A callback for the user to save a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="954ba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="954ba-105">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="954ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="954ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="954ba-107">*pXofSave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="954ba-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="954ba-108">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="954ba-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="954ba-109">Ponteiro para um arquivo. x salvar objeto.</span><span class="sxs-lookup"><span data-stu-id="954ba-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="954ba-110">Não use esse parâmetro para adicionar objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="954ba-110">Do not use this parameter to add data objects.</span></span> <span data-ttu-id="954ba-111">Consulte [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span><span class="sxs-lookup"><span data-stu-id="954ba-111">See [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="954ba-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="954ba-112">Return value</span></span>

<span data-ttu-id="954ba-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="954ba-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="954ba-114">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="954ba-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="954ba-115">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="954ba-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="954ba-116">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="954ba-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="954ba-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="954ba-117">Remarks</span></span>

<span data-ttu-id="954ba-118">[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) e **ID3DXSaveUserData:: SaveTemplates** fornecem um mecanismo para adicionar um modelo a um arquivo. x para salvar dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="954ba-118">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and **ID3DXSaveUserData::SaveTemplates** provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="954ba-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="954ba-119">Requirements</span></span>



| <span data-ttu-id="954ba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="954ba-120">Requirement</span></span> | <span data-ttu-id="954ba-121">Valor</span><span class="sxs-lookup"><span data-stu-id="954ba-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="954ba-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="954ba-122">Header</span></span><br/>  | <dl> <span data-ttu-id="954ba-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="954ba-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="954ba-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="954ba-124">Library</span></span><br/> | <dl> <span data-ttu-id="954ba-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="954ba-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="954ba-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="954ba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="954ba-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="954ba-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
