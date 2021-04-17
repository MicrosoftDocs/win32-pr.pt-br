---
description: Um retorno de chamada para o usuário registrar um modelo de arquivo. x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'Método ID3DXSaveUserData:: RegisterTemplates (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812389"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a><span data-ttu-id="6ca81-103">Método ID3DXSaveUserData:: RegisterTemplates</span><span class="sxs-lookup"><span data-stu-id="6ca81-103">ID3DXSaveUserData::RegisterTemplates method</span></span>

<span data-ttu-id="6ca81-104">Um retorno de chamada para o usuário registrar um modelo de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="6ca81-104">A callback for the user to register a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca81-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ca81-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a><span data-ttu-id="6ca81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ca81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca81-107">*pXFileApi* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ca81-107">*pXFileApi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca81-108">Tipo: **[ **LPD3DXFILE**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="6ca81-108">Type: **[**LPD3DXFILE**](id3dxfile.md)**</span></span>

<span data-ttu-id="6ca81-109">Use esse ponteiro para registrar modelos de arquivo. x definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6ca81-109">Use this pointer to register user-defined .x file templates.</span></span> <span data-ttu-id="6ca81-110">Consulte [**ID3DXFile**](id3dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="6ca81-110">See [**ID3DXFile**](id3dxfile.md).</span></span> <span data-ttu-id="6ca81-111">Não use esse parâmetro para adicionar objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="6ca81-111">Do not use this parameter to add data objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca81-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ca81-112">Return value</span></span>

<span data-ttu-id="6ca81-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ca81-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ca81-114">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6ca81-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="6ca81-115">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ca81-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="6ca81-116">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="6ca81-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca81-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ca81-117">Remarks</span></span>

<span data-ttu-id="6ca81-118">**ID3DXSaveUserData:: RegisterTemplates** e [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fornecem um mecanismo para adicionar um modelo a um arquivo. x para salvar dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ca81-118">**ID3DXSaveUserData::RegisterTemplates** and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca81-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ca81-119">Requirements</span></span>



| <span data-ttu-id="6ca81-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ca81-120">Requirement</span></span> | <span data-ttu-id="6ca81-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6ca81-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca81-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ca81-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6ca81-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca81-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6ca81-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ca81-124">Library</span></span><br/> | <dl> <span data-ttu-id="6ca81-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ca81-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ca81-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ca81-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca81-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="6ca81-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
