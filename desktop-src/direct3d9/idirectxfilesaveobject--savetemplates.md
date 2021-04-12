---
description: Salva modelos em um arquivo do DirectX. Preterido.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Método IDirectXFileSaveObject:: SaveTemplates (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298583"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a><span data-ttu-id="4394c-104">Método IDirectXFileSaveObject:: SaveTemplates</span><span class="sxs-lookup"><span data-stu-id="4394c-104">IDirectXFileSaveObject::SaveTemplates method</span></span>

<span data-ttu-id="4394c-105">Salva modelos em um arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="4394c-105">Saves templates to a DirectX file.</span></span> <span data-ttu-id="4394c-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="4394c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4394c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4394c-107">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a><span data-ttu-id="4394c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4394c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4394c-109">*cTemplates* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4394c-109">*cTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4394c-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4394c-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4394c-111">Número total de modelos a serem salvos.</span><span class="sxs-lookup"><span data-stu-id="4394c-111">Total number of templates to save.</span></span>

</dd> <dt>

<span data-ttu-id="4394c-112">*ppguidTemplates* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4394c-112">*ppguidTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4394c-113">Tipo: **[**GUID**](guid.md) \* \* const**</span><span class="sxs-lookup"><span data-stu-id="4394c-113">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="4394c-114">Endereço de um ponteiro para uma matriz de GUIDs para todos os modelos a serem salvos.</span><span class="sxs-lookup"><span data-stu-id="4394c-114">Address of a pointer to an array of the GUIDs for all templates to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4394c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4394c-115">Return value</span></span>

<span data-ttu-id="4394c-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4394c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4394c-117">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4394c-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="4394c-118">Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="4394c-118">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="4394c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4394c-119">Remarks</span></span>

<span data-ttu-id="4394c-120">O fragmento de código a seguir fornece uma chamada de exemplo para **IDirectXFileSaveObject:: SaveTemplates** e conteúdo de exemplo para a matriz para a qual ppguidTemplates aponta.</span><span class="sxs-lookup"><span data-stu-id="4394c-120">The following code fragment provides an example call to **IDirectXFileSaveObject::SaveTemplates** and example contents for the array to which ppguidTemplates points.</span></span>


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



<span data-ttu-id="4394c-121">Depois de usar esse método para salvar os modelos, use o método [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar um objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="4394c-121">After using this method to save the templates, use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4394c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4394c-122">Requirements</span></span>



| <span data-ttu-id="4394c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4394c-123">Requirement</span></span> | <span data-ttu-id="4394c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4394c-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4394c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4394c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4394c-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4394c-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="4394c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4394c-127">Library</span></span><br/> | <dl> <span data-ttu-id="4394c-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4394c-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4394c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4394c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4394c-130">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="4394c-130">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="4394c-131">**IDirectXFileSaveObject:: createdataobject**</span><span class="sxs-lookup"><span data-stu-id="4394c-131">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
