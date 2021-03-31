---
description: Cria um objeto enumerador. Preterido.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'Método IDirectXFile:: createenumobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664072"
---
# <a name="idirectxfilecreateenumobject-method"></a><span data-ttu-id="48717-104">Método IDirectXFile:: createenumobject</span><span class="sxs-lookup"><span data-stu-id="48717-104">IDirectXFile::CreateEnumObject method</span></span>

<span data-ttu-id="48717-105">Cria um objeto enumerador.</span><span class="sxs-lookup"><span data-stu-id="48717-105">Creates an enumerator object.</span></span> <span data-ttu-id="48717-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="48717-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="48717-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48717-107">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="48717-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48717-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48717-109">*pvSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48717-109">*pvSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48717-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48717-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48717-111">Ponteiro para dados cujos conteúdos dependem do valor de dwLoadOptions</span><span class="sxs-lookup"><span data-stu-id="48717-111">Pointer to data whose contents depend on the value of dwLoadOptions</span></span>

</dd> <dt>

<span data-ttu-id="48717-112">*dwLoadOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48717-112">*dwLoadOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48717-113">Tipo: **[ **DXFILELOADOPTIONS**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="48717-113">Type: **[**DXFILELOADOPTIONS**](dxfile.md)**</span></span>

<span data-ttu-id="48717-114">Valor que especifica a origem dos dados.</span><span class="sxs-lookup"><span data-stu-id="48717-114">Value that specifies the source of the data.</span></span> <span data-ttu-id="48717-115">Esse valor pode ser um dos sinalizadores DXFILELOAD \_ XXX em [constantes DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="48717-115">This value can be one of the DXFILELOAD\_xxx flags in [DXFILE Constants](dxfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="48717-116">*ppEnumObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="48717-116">*ppEnumObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="48717-117">Tipo: **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="48717-117">Type: **[**LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span></span>

<span data-ttu-id="48717-118">Endereço de um ponteiro para uma interface [**IDirectXFileEnumObject**](idirectxfileenumobject.md) , que representa o objeto enumerador criado.</span><span class="sxs-lookup"><span data-stu-id="48717-118">Address of a pointer to an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48717-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48717-119">Return value</span></span>

<span data-ttu-id="48717-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48717-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48717-121">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48717-121">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="48717-122">Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="48717-122">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADRESOURCE, DXFILEERR\_BADVALUE, DXFILEERR\_FILENOTFOUND, DXFILEERR\_RESOURCENOTFOUND, DXFILEERR\_URLNOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="48717-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="48717-123">Remarks</span></span>

<span data-ttu-id="48717-124">Depois de usar esse método, use um dos métodos IDirectXFileEnumObject para recuperar um objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="48717-124">After using this method, use one of the IDirectXFileEnumObject methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="48717-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48717-125">Requirements</span></span>



| <span data-ttu-id="48717-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="48717-126">Requirement</span></span> | <span data-ttu-id="48717-127">Valor</span><span class="sxs-lookup"><span data-stu-id="48717-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48717-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48717-128">Header</span></span><br/>  | <dl> <span data-ttu-id="48717-129"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="48717-129"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="48717-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48717-130">Library</span></span><br/> | <dl> <span data-ttu-id="48717-131"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48717-131"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48717-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="48717-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48717-133">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="48717-133">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
