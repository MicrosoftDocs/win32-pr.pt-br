---
description: Resolve referências de dados. Preterido.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'Método IDirectXFileDataReference:: resolve (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812207"
---
# <a name="idirectxfiledatareferenceresolve-method"></a><span data-ttu-id="81734-104">Método IDirectXFileDataReference:: resolve</span><span class="sxs-lookup"><span data-stu-id="81734-104">IDirectXFileDataReference::Resolve method</span></span>

<span data-ttu-id="81734-105">Resolve referências de dados.</span><span class="sxs-lookup"><span data-stu-id="81734-105">Resolves data references.</span></span> <span data-ttu-id="81734-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="81734-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="81734-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81734-107">Syntax</span></span>


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="81734-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81734-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81734-109">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="81734-109">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="81734-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="81734-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="81734-111">Endereço de um ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , que representa o objeto de dados de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="81734-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81734-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81734-112">Return value</span></span>

<span data-ttu-id="81734-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81734-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81734-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81734-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="81734-115">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="81734-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="81734-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81734-116">Requirements</span></span>



| <span data-ttu-id="81734-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81734-117">Requirement</span></span> | <span data-ttu-id="81734-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81734-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81734-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81734-119">Header</span></span><br/>  | <dl> <span data-ttu-id="81734-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="81734-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="81734-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81734-121">Library</span></span><br/> | <dl> <span data-ttu-id="81734-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81734-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81734-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="81734-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81734-124">IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="81734-124">IDirectXFileDataReference</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




