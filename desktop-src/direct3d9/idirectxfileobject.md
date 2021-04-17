---
description: Os aplicativos usam os métodos da interface IDirectXFileObject para recuperar informações sobre objetos de arquivo do Microsoft DirectX. Preterido.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interface IDirectXFileObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762061"
---
# <a name="idirectxfileobject-interface"></a><span data-ttu-id="9d378-104">Interface IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="9d378-104">IDirectXFileObject interface</span></span>

<span data-ttu-id="9d378-105">Os aplicativos usam os métodos da interface IDirectXFileObject para recuperar informações sobre objetos de arquivo do Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="9d378-105">Applications use the methods of the IDirectXFileObject interface to retrieve information about Microsoft DirectX file objects.</span></span> <span data-ttu-id="9d378-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9d378-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="9d378-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9d378-107">Members</span></span>

<span data-ttu-id="9d378-108">A interface **IDirectXFileObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9d378-108">The **IDirectXFileObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9d378-109">**IDirectXFileObject** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9d378-109">**IDirectXFileObject** also has these types of members:</span></span>

-   [<span data-ttu-id="9d378-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d378-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9d378-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d378-111">Methods</span></span>

<span data-ttu-id="9d378-112">A interface **IDirectXFileObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9d378-112">The **IDirectXFileObject** interface has these methods.</span></span>



| <span data-ttu-id="9d378-113">Método</span><span class="sxs-lookup"><span data-stu-id="9d378-113">Method</span></span>                                         | <span data-ttu-id="9d378-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d378-114">Description</span></span>                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d378-115">**GetId**</span><span class="sxs-lookup"><span data-stu-id="9d378-115">**GetId**</span></span>](idirectxfileobject--getid.md)     | <span data-ttu-id="9d378-116">Recupera um ponteiro para o GUID que identifica um objeto de arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="9d378-116">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="9d378-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9d378-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="9d378-118">**GetName**</span><span class="sxs-lookup"><span data-stu-id="9d378-118">**GetName**</span></span>](idirectxfileobject--getname.md) | <span data-ttu-id="9d378-119">Recupera um ponteiro para o nome de um objeto de arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="9d378-119">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="9d378-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9d378-120">Deprecated.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="9d378-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d378-121">Remarks</span></span>

<span data-ttu-id="9d378-122">O GUID da interface IDirectXFileObject é IDirectXFileObject IID \_ .</span><span class="sxs-lookup"><span data-stu-id="9d378-122">The GUID for the IDirectXFileObject interface is IID\_IDirectXFileObject.</span></span>

<span data-ttu-id="9d378-123">O tipo LPDIRECTXFILEOBJECT é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="9d378-123">The LPDIRECTXFILEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="9d378-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d378-124">Requirements</span></span>



| <span data-ttu-id="9d378-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d378-125">Requirement</span></span> | <span data-ttu-id="9d378-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9d378-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d378-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d378-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9d378-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d378-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d378-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d378-129">Library</span></span><br/> | <dl> <span data-ttu-id="9d378-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d378-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d378-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d378-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d378-132">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="9d378-132">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
