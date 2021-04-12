---
description: Recupera o próximo objeto de nível superior no arquivo do DirectX. Preterido.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'Método IDirectXFileEnumObject:: GetNextDataObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298495"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a><span data-ttu-id="d5e35-104">Método IDirectXFileEnumObject:: GetNextDataObject</span><span class="sxs-lookup"><span data-stu-id="d5e35-104">IDirectXFileEnumObject::GetNextDataObject method</span></span>

<span data-ttu-id="d5e35-105">Recupera o próximo objeto de nível superior no arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="d5e35-105">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="d5e35-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="d5e35-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e35-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5e35-107">Syntax</span></span>


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="d5e35-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5e35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e35-109">*ppDataObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5e35-109">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e35-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5e35-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="d5e35-111">Endereço de um ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , que representa o objeto de dados de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="d5e35-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e35-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5e35-112">Return value</span></span>

<span data-ttu-id="d5e35-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5e35-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5e35-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5e35-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d5e35-115">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d5e35-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e35-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5e35-116">Remarks</span></span>

<span data-ttu-id="d5e35-117">Os objetos de nível superior são sempre objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="d5e35-117">Top-level objects are always data objects.</span></span> <span data-ttu-id="d5e35-118">Objetos de referência de dados e objetos binários só podem ser filhos de objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="d5e35-118">Data reference objects and binary objects can only be children of data objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e35-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e35-119">Requirements</span></span>



| <span data-ttu-id="d5e35-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e35-120">Requirement</span></span> | <span data-ttu-id="d5e35-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d5e35-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e35-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5e35-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d5e35-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e35-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5e35-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5e35-124">Library</span></span><br/> | <dl> <span data-ttu-id="d5e35-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5e35-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e35-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5e35-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e35-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="d5e35-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 




