---
description: Adiciona um objeto de dados como um filho do nó de dados do arquivo ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'Método ID3DXFileSaveData:: adddataobject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298693"
---
# <a name="id3dxfilesavedataadddataobject-method"></a><span data-ttu-id="093be-103">Método ID3DXFileSaveData:: adddataobject</span><span class="sxs-lookup"><span data-stu-id="093be-103">ID3DXFileSaveData::AddDataObject method</span></span>

<span data-ttu-id="093be-104">Adiciona um objeto de dados como um filho do nó de dados do arquivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="093be-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="093be-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="093be-105">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="093be-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="093be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="093be-107">*rguidTemplate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="093be-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093be-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="093be-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="093be-109">GUID que representa o modelo do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="093be-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="093be-110">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="093be-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093be-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="093be-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="093be-112">Ponteiro para o nome do objeto de dados a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="093be-112">Pointer to the name of the data object to add.</span></span> <span data-ttu-id="093be-113">Especifique **NULL** se o objeto não tiver um nome.</span><span class="sxs-lookup"><span data-stu-id="093be-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="093be-114">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="093be-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093be-115">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="093be-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="093be-116">Ponteiro para um GUID que representa o objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="093be-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="093be-117">O objeto de dados deve ter sido registrado com [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) ou [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span><span class="sxs-lookup"><span data-stu-id="093be-117">The data object must have been registered with [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) or [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span></span> <span data-ttu-id="093be-118">Especifique **NULL** se o objeto não tiver um GUID.</span><span class="sxs-lookup"><span data-stu-id="093be-118">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="093be-119">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="093be-119">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093be-120">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="093be-120">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="093be-121">Tamanho do objeto de dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="093be-121">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="093be-122">*pvData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="093be-122">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093be-123">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="093be-123">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="093be-124">Ponteiro para um buffer que contém todos os dados necessários no objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="093be-124">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="093be-125">*ppObj* \[ no, retval\]</span><span class="sxs-lookup"><span data-stu-id="093be-125">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="093be-126">Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="093be-126">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="093be-127">Endereço de um ponteiro para uma interface [**ID3DXFileSaveData**](id3dxfilesavedata.md) , que representa o nó de dados do arquivo ao qual o objeto de dados será adicionado.</span><span class="sxs-lookup"><span data-stu-id="093be-127">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="093be-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="093be-128">Return value</span></span>

<span data-ttu-id="093be-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="093be-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="093be-130">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="093be-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="093be-131">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="093be-131">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="093be-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="093be-132">Requirements</span></span>



| <span data-ttu-id="093be-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="093be-133">Requirement</span></span> | <span data-ttu-id="093be-134">Valor</span><span class="sxs-lookup"><span data-stu-id="093be-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="093be-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="093be-135">Header</span></span><br/>  | <dl> <span data-ttu-id="093be-136"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="093be-136"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="093be-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="093be-137">Library</span></span><br/> | <dl> <span data-ttu-id="093be-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="093be-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="093be-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="093be-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="093be-140">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="093be-140">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
