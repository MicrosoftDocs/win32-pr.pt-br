---
description: Recupera o próximo objeto de dados filho, objeto de referência de dados ou objeto binário no arquivo do DirectX. Preterido.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Método IDirectXFileData:: GetNextObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814175"
---
# <a name="idirectxfiledatagetnextobject-method"></a><span data-ttu-id="39331-104">Método IDirectXFileData:: GetNextObject</span><span class="sxs-lookup"><span data-stu-id="39331-104">IDirectXFileData::GetNextObject method</span></span>

<span data-ttu-id="39331-105">Recupera o próximo objeto de dados filho, objeto de referência de dados ou objeto binário no arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="39331-105">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="39331-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="39331-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="39331-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39331-107">Syntax</span></span>


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a><span data-ttu-id="39331-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39331-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39331-109">*ppChildObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="39331-109">*ppChildObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="39331-110">Tipo: **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="39331-110">Type: **[**LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span></span>

<span data-ttu-id="39331-111">Endereço de um ponteiro para uma interface [**IDirectXFileObject**](idirectxfileobject.md) , que representa a interface de objeto de arquivo do objeto filho retornado.</span><span class="sxs-lookup"><span data-stu-id="39331-111">Address of a pointer to an [**IDirectXFileObject**](idirectxfileobject.md) interface, representing the returned child object's file object interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39331-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39331-112">Return value</span></span>

<span data-ttu-id="39331-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39331-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39331-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="39331-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="39331-115">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="39331-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="39331-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="39331-116">Remarks</span></span>

<span data-ttu-id="39331-117">Para determinar o tipo de objeto recuperado, use QueryInterface para consultar o objeto recuperado para oferecer suporte às interfaces [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md)ou [**IDirectXFileBinary**](idirectxfilebinary.md) .</span><span class="sxs-lookup"><span data-stu-id="39331-117">To determine the type of object retrieved, use QueryInterface to query the retrieved object for support of [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md) interfaces.</span></span> <span data-ttu-id="39331-118">A interface suportada indica o tipo de objeto (dados, referência de dados ou binário).</span><span class="sxs-lookup"><span data-stu-id="39331-118">The interface supported indicates the type of object (data, data reference, or binary).</span></span>

## <a name="requirements"></a><span data-ttu-id="39331-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39331-119">Requirements</span></span>



| <span data-ttu-id="39331-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="39331-120">Requirement</span></span> | <span data-ttu-id="39331-121">Valor</span><span class="sxs-lookup"><span data-stu-id="39331-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39331-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39331-122">Header</span></span><br/>  | <dl> <span data-ttu-id="39331-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="39331-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="39331-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39331-124">Library</span></span><br/> | <dl> <span data-ttu-id="39331-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39331-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39331-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="39331-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39331-127">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="39331-127">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
</dt> <dt>

[<span data-ttu-id="39331-128">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="39331-128">**IDirectXFileData**</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="39331-129">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="39331-129">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




