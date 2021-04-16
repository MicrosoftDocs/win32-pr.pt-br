---
description: Recupera o objeto de dados que tem o nome especificado. Preterido.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'Método IDirectXFileEnumObject:: GetDataObjectByName (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768395"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="ed0ac-104">Método IDirectXFileEnumObject:: GetDataObjectByName</span><span class="sxs-lookup"><span data-stu-id="ed0ac-104">IDirectXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="ed0ac-105">Recupera o objeto de dados que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="ed0ac-105">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="ed0ac-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="ed0ac-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed0ac-107">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="ed0ac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed0ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed0ac-109">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed0ac-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed0ac-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed0ac-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed0ac-111">Ponteiro para o nome solicitado.</span><span class="sxs-lookup"><span data-stu-id="ed0ac-111">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="ed0ac-112">*ppDataObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed0ac-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed0ac-113">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed0ac-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="ed0ac-114">Endereço de um ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , que representa o objeto de dados de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="ed0ac-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed0ac-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed0ac-115">Return value</span></span>

<span data-ttu-id="ed0ac-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed0ac-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed0ac-117">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed0ac-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ed0ac-118">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="ed0ac-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed0ac-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed0ac-119">Requirements</span></span>



| <span data-ttu-id="ed0ac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed0ac-120">Requirement</span></span> | <span data-ttu-id="ed0ac-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ed0ac-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0ac-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed0ac-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ed0ac-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed0ac-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed0ac-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed0ac-124">Library</span></span><br/> | <dl> <span data-ttu-id="ed0ac-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed0ac-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed0ac-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed0ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed0ac-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="ed0ac-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
