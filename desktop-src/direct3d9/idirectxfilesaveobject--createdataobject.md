---
description: Cria um objeto de dados. Preterido.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'Método IDirectXFileSaveObject:: createdataobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298584"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a><span data-ttu-id="d7963-104">Método IDirectXFileSaveObject:: createdataobject</span><span class="sxs-lookup"><span data-stu-id="d7963-104">IDirectXFileSaveObject::CreateDataObject method</span></span>

<span data-ttu-id="d7963-105">Cria um objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="d7963-105">Creates a data object.</span></span> <span data-ttu-id="d7963-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="d7963-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7963-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7963-107">Syntax</span></span>


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="d7963-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7963-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7963-109">*rguidTemplate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7963-109">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7963-110">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="d7963-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="d7963-111">GUID que representa o modelo do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="d7963-111">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="d7963-112">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7963-112">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7963-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7963-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7963-114">Ponteiro para o nome do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="d7963-114">Pointer to the name of the data object.</span></span> <span data-ttu-id="d7963-115">Especifique **NULL** se o objeto não tiver um nome.</span><span class="sxs-lookup"><span data-stu-id="d7963-115">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="d7963-116">*pGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7963-116">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7963-117">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="d7963-117">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="d7963-118">Ponteiro para um GUID que representa o objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="d7963-118">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="d7963-119">Especifique **NULL** se o objeto não tiver um GUID.</span><span class="sxs-lookup"><span data-stu-id="d7963-119">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="d7963-120">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7963-120">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7963-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7963-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7963-122">Tamanho do objeto de dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d7963-122">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d7963-123">*pvData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7963-123">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7963-124">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7963-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7963-125">Ponteiro para um buffer que contém todos os dados do membro necessário.</span><span class="sxs-lookup"><span data-stu-id="d7963-125">Pointer to a buffer containing all required member's data.</span></span>

</dd> <dt>

<span data-ttu-id="d7963-126">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d7963-126">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d7963-127">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7963-127">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="d7963-128">Endereço de um ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , que representa o objeto de dados de arquivo criado.</span><span class="sxs-lookup"><span data-stu-id="d7963-128">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the created file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7963-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7963-129">Return value</span></span>

<span data-ttu-id="d7963-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7963-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7963-131">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d7963-131">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d7963-132">Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="d7963-132">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="d7963-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7963-133">Remarks</span></span>

<span data-ttu-id="d7963-134">Se um objeto de referência de dados fizer referência ao objeto de dados, o parâmetro szName ou pGuid deverá ser não **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d7963-134">If a data reference object will reference the data object, either the szName or pguid parameter must be non-**NULL**.</span></span>

<span data-ttu-id="d7963-135">Salve todos os modelos usando o método [**IDirectXFileSaveObject:: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) antes de salvar os dados criados por esse método.</span><span class="sxs-lookup"><span data-stu-id="d7963-135">Save any templates by using the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method before saving the data created by this method.</span></span> <span data-ttu-id="d7963-136">Salve os dados criados usando o método [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) .</span><span class="sxs-lookup"><span data-stu-id="d7963-136">Save the created data by using the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method.</span></span>

<span data-ttu-id="d7963-137">Se você precisar salvar dados opcionais, use o método [**IDirectXFileData:: Adddataobject**](idirectxfiledata--adddataobject.md) depois de usar esse método e antes de usar [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md).</span><span class="sxs-lookup"><span data-stu-id="d7963-137">If you need to save optional data, use the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method after using this method and before using [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md).</span></span> <span data-ttu-id="d7963-138">Se o objeto tiver objetos filho, adicione-os antes de chamar **IDirectXFileSaveObject:: SaveData**.</span><span class="sxs-lookup"><span data-stu-id="d7963-138">If the object has child objects, add them before calling **IDirectXFileSaveObject::SaveData**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7963-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7963-139">Requirements</span></span>



| <span data-ttu-id="d7963-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7963-140">Requirement</span></span> | <span data-ttu-id="d7963-141">Valor</span><span class="sxs-lookup"><span data-stu-id="d7963-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7963-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7963-142">Header</span></span><br/>  | <dl> <span data-ttu-id="d7963-143"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7963-143"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7963-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7963-144">Library</span></span><br/> | <dl> <span data-ttu-id="d7963-145"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7963-145"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7963-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7963-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7963-147">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="d7963-147">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="d7963-148">**IDirectXFileData:: adddataobject**</span><span class="sxs-lookup"><span data-stu-id="d7963-148">**IDirectXFileData::AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)
</dt> <dt>

[<span data-ttu-id="d7963-149">**IDirectXFileSaveObject:: SaveData**</span><span class="sxs-lookup"><span data-stu-id="d7963-149">**IDirectXFileSaveObject::SaveData**</span></span>](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[<span data-ttu-id="d7963-150">**IDirectXFileSaveObject::SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="d7963-150">**IDirectXFileSaveObject::SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
