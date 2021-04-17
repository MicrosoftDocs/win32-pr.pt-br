---
description: Recupera o objeto de dados que tem o GUID especificado. Preterido.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'Método IDirectXFileEnumObject:: GetDataObjectById (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811720"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="2cbc9-104">Método IDirectXFileEnumObject:: GetDataObjectById</span><span class="sxs-lookup"><span data-stu-id="2cbc9-104">IDirectXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="2cbc9-105">Recupera o objeto de dados que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="2cbc9-105">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="2cbc9-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="2cbc9-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbc9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cbc9-107">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="2cbc9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cbc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbc9-109">*rguid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cbc9-109">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbc9-110">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="2cbc9-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="2cbc9-111">Referência ao GUID solicitado.</span><span class="sxs-lookup"><span data-stu-id="2cbc9-111">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc9-112">*ppDataObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2cbc9-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbc9-113">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cbc9-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="2cbc9-114">Endereço de um ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , que representa o objeto de dados de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="2cbc9-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbc9-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cbc9-115">Return value</span></span>

<span data-ttu-id="2cbc9-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2cbc9-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2cbc9-117">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2cbc9-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="2cbc9-118">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="2cbc9-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbc9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cbc9-119">Requirements</span></span>



| <span data-ttu-id="2cbc9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cbc9-120">Requirement</span></span> | <span data-ttu-id="2cbc9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2cbc9-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbc9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2cbc9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2cbc9-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc9-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cbc9-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cbc9-124">Library</span></span><br/> | <dl> <span data-ttu-id="2cbc9-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc9-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cbc9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cbc9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbc9-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="2cbc9-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
