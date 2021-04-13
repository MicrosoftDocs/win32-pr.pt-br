---
description: Adiciona um objeto de dados como um objeto filho. Preterido.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'Método IDirectXFileData:: adddataobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298729"
---
# <a name="idirectxfiledataadddataobject-method"></a><span data-ttu-id="ac05c-104">Método IDirectXFileData:: adddataobject</span><span class="sxs-lookup"><span data-stu-id="ac05c-104">IDirectXFileData::AddDataObject method</span></span>

<span data-ttu-id="ac05c-105">Adiciona um objeto de dados como um objeto filho.</span><span class="sxs-lookup"><span data-stu-id="ac05c-105">Adds a data object as a child object.</span></span> <span data-ttu-id="ac05c-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="ac05c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac05c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac05c-107">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="ac05c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac05c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac05c-109">*pDataObj* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac05c-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac05c-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="ac05c-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="ac05c-111">Ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , representando o objeto de dados de arquivo a ser adicionado como um objeto filho.</span><span class="sxs-lookup"><span data-stu-id="ac05c-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to add as a child object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac05c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac05c-112">Return value</span></span>

<span data-ttu-id="ac05c-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac05c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac05c-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac05c-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ac05c-115">Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="ac05c-115">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="ac05c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac05c-116">Remarks</span></span>

<span data-ttu-id="ac05c-117">Use o método [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar o objeto [**IDirectXFileData**](idirectxfiledata.md) antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="ac05c-117">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create the [**IDirectXFileData**](idirectxfiledata.md) object before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac05c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac05c-118">Requirements</span></span>



| <span data-ttu-id="ac05c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac05c-119">Requirement</span></span> | <span data-ttu-id="ac05c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ac05c-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac05c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac05c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ac05c-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac05c-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac05c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac05c-123">Library</span></span><br/> | <dl> <span data-ttu-id="ac05c-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac05c-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac05c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac05c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac05c-126">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="ac05c-126">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="ac05c-127">**IDirectXFileSaveObject:: createdataobject**</span><span class="sxs-lookup"><span data-stu-id="ac05c-127">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




