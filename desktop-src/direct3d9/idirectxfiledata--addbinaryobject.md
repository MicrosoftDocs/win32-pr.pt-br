---
description: Cria um objeto binário e o adiciona como um objeto filho. Preterido.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'Método IDirectXFileData:: addbinaryobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172931"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a><span data-ttu-id="4768b-104">Método IDirectXFileData:: addbinaryobject</span><span class="sxs-lookup"><span data-stu-id="4768b-104">IDirectXFileData::AddBinaryObject method</span></span>

<span data-ttu-id="4768b-105">Cria um objeto binário e o adiciona como um objeto filho.</span><span class="sxs-lookup"><span data-stu-id="4768b-105">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="4768b-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="4768b-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4768b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4768b-107">Syntax</span></span>


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="4768b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4768b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4768b-109">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4768b-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4768b-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4768b-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4768b-111">Ponteiro para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="4768b-111">Pointer to the name of the object.</span></span> <span data-ttu-id="4768b-112">Especifique **NULL** se o objeto não precisar de um nome.</span><span class="sxs-lookup"><span data-stu-id="4768b-112">Specify **NULL** if the object does not need a name.</span></span>

</dd> <dt>

<span data-ttu-id="4768b-113">*pGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4768b-113">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4768b-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="4768b-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="4768b-115">Ponteiro para o GUID que representa o objeto.</span><span class="sxs-lookup"><span data-stu-id="4768b-115">Pointer to the GUID representing the object.</span></span> <span data-ttu-id="4768b-116">Especifique **NULL** se o objeto não precisar de um GUID.</span><span class="sxs-lookup"><span data-stu-id="4768b-116">Specify **NULL** if the object does not need a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="4768b-117">*szMimeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4768b-117">*szMimeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4768b-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4768b-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4768b-119">Ponteiro para o tipo MIME do objeto.</span><span class="sxs-lookup"><span data-stu-id="4768b-119">Pointer to the object's MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="4768b-120">*pvData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4768b-120">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4768b-121">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4768b-121">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4768b-122">Ponteiro para os dados do objeto.</span><span class="sxs-lookup"><span data-stu-id="4768b-122">Pointer to the object's data.</span></span>

</dd> <dt>

<span data-ttu-id="4768b-123">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4768b-123">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4768b-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4768b-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4768b-125">Tamanho do buffer apontado por pvData, em bytes.</span><span class="sxs-lookup"><span data-stu-id="4768b-125">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4768b-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4768b-126">Return value</span></span>

<span data-ttu-id="4768b-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4768b-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4768b-128">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4768b-128">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="4768b-129">Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="4768b-129">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="4768b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4768b-130">Requirements</span></span>



| <span data-ttu-id="4768b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4768b-131">Requirement</span></span> | <span data-ttu-id="4768b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4768b-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4768b-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4768b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4768b-134"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4768b-134"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="4768b-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4768b-135">Library</span></span><br/> | <dl> <span data-ttu-id="4768b-136"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4768b-136"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4768b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4768b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4768b-138">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="4768b-138">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="4768b-139">**IDirectXFileBinary:: getMimeType**</span><span class="sxs-lookup"><span data-stu-id="4768b-139">**IDirectXFileBinary::GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
