---
description: Os aplicativos usam os métodos da interface IDirectXFile para criar instâncias das interfaces IDirectXFileEnumObject e IDirectXFileSaveObject e para registrar modelos. Preterido.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interface IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837968"
---
# <a name="idirectxfile-interface"></a><span data-ttu-id="54ab6-104">Interface IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="54ab6-104">IDirectXFile interface</span></span>

<span data-ttu-id="54ab6-105">Os aplicativos usam os métodos da interface IDirectXFile para criar instâncias das interfaces [**IDirectXFileEnumObject**](idirectxfileenumobject.md) e [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) e para registrar modelos.</span><span class="sxs-lookup"><span data-stu-id="54ab6-105">Applications use the methods of the IDirectXFile interface to create instances of the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) and [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interfaces, and to register templates.</span></span> <span data-ttu-id="54ab6-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="54ab6-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="54ab6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="54ab6-107">Members</span></span>

<span data-ttu-id="54ab6-108">A interface **IDirectXFile** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="54ab6-108">The **IDirectXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="54ab6-109">**IDirectXFile** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="54ab6-109">**IDirectXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="54ab6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="54ab6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54ab6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="54ab6-111">Methods</span></span>

<span data-ttu-id="54ab6-112">A interface **IDirectXFile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="54ab6-112">The **IDirectXFile** interface has these methods.</span></span>



| <span data-ttu-id="54ab6-113">Método</span><span class="sxs-lookup"><span data-stu-id="54ab6-113">Method</span></span>                                                       | <span data-ttu-id="54ab6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="54ab6-114">Description</span></span>                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="54ab6-115">**Createenumobject**</span><span class="sxs-lookup"><span data-stu-id="54ab6-115">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)   | <span data-ttu-id="54ab6-116">Cria um objeto enumerador.</span><span class="sxs-lookup"><span data-stu-id="54ab6-116">Creates an enumerator object.</span></span> <span data-ttu-id="54ab6-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="54ab6-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="54ab6-118">**Createsaveobject**</span><span class="sxs-lookup"><span data-stu-id="54ab6-118">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)   | <span data-ttu-id="54ab6-119">Cria um objeto salvar.</span><span class="sxs-lookup"><span data-stu-id="54ab6-119">Creates a save object.</span></span> <span data-ttu-id="54ab6-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="54ab6-120">Deprecated.</span></span><br/>        |
| [<span data-ttu-id="54ab6-121">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="54ab6-121">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md) | <span data-ttu-id="54ab6-122">Registra modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="54ab6-122">Registers custom templates.</span></span> <span data-ttu-id="54ab6-123">Preterido.</span><span class="sxs-lookup"><span data-stu-id="54ab6-123">Deprecated.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="54ab6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="54ab6-124">Remarks</span></span>

<span data-ttu-id="54ab6-125">O GUID (identificador global exclusivo) da interface IDirectXFile é IDirectXFile de IID \_ .</span><span class="sxs-lookup"><span data-stu-id="54ab6-125">The globally unique identifier (GUID) for the IDirectXFile interface is IID\_IDirectXFile.</span></span>

<span data-ttu-id="54ab6-126">A interface IDirectXFile é obtida chamando a função [**DirectXFileCreate**](directxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="54ab6-126">The IDirectXFile interface is obtained by calling the [**DirectXFileCreate**](directxfilecreate.md) function.</span></span>

<span data-ttu-id="54ab6-127">O tipo LPDIRECTXFILE é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="54ab6-127">The LPDIRECTXFILE type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a><span data-ttu-id="54ab6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54ab6-128">Requirements</span></span>



| <span data-ttu-id="54ab6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ab6-129">Requirement</span></span> | <span data-ttu-id="54ab6-130">Valor</span><span class="sxs-lookup"><span data-stu-id="54ab6-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54ab6-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54ab6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="54ab6-132"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="54ab6-132"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="54ab6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54ab6-133">Library</span></span><br/> | <dl> <span data-ttu-id="54ab6-134"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54ab6-134"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ab6-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="54ab6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ab6-136">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="54ab6-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
