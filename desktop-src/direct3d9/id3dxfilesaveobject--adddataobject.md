---
description: Adiciona um objeto de dados como um filho do objeto ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'Método ID3DXFileSaveObject:: adddataobject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798189"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a><span data-ttu-id="46ee4-103">Método ID3DXFileSaveObject:: adddataobject</span><span class="sxs-lookup"><span data-stu-id="46ee4-103">ID3DXFileSaveObject::AddDataObject method</span></span>

<span data-ttu-id="46ee4-104">Adiciona um objeto de dados como um filho do objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="46ee4-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ee4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46ee4-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="46ee4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46ee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ee4-107">*rguidTemplate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ee4-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ee4-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="46ee4-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="46ee4-109">GUID que representa o modelo do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="46ee4-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="46ee4-110">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ee4-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ee4-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ee4-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ee4-112">Ponteiro para o nome do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="46ee4-112">Pointer to the name of the data object.</span></span> <span data-ttu-id="46ee4-113">Especifique **NULL** se o objeto não tiver um nome.</span><span class="sxs-lookup"><span data-stu-id="46ee4-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="46ee4-114">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ee4-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ee4-115">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="46ee4-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="46ee4-116">Ponteiro para um GUID que representa o objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="46ee4-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="46ee4-117">Especifique **NULL** se o objeto não tiver um GUID.</span><span class="sxs-lookup"><span data-stu-id="46ee4-117">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="46ee4-118">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ee4-118">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ee4-119">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ee4-119">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ee4-120">Tamanho do objeto de dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="46ee4-120">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="46ee4-121">*pvData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ee4-121">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ee4-122">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ee4-122">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ee4-123">Ponteiro para um buffer que contém todos os dados necessários no objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="46ee4-123">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="46ee4-124">*ppObj* \[ no, retval\]</span><span class="sxs-lookup"><span data-stu-id="46ee4-124">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="46ee4-125">Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="46ee4-125">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="46ee4-126">Endereço de um ponteiro para uma interface [**ID3DXFileSaveData**](id3dxfilesavedata.md) , que representa o nó de dados do arquivo ao qual o objeto de dados será adicionado.</span><span class="sxs-lookup"><span data-stu-id="46ee4-126">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ee4-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46ee4-127">Return value</span></span>

<span data-ttu-id="46ee4-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46ee4-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46ee4-129">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46ee4-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="46ee4-130">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="46ee4-130">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, DXFILEERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ee4-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="46ee4-131">Remarks</span></span>

<span data-ttu-id="46ee4-132">Se um objeto de referência de dados fizer referência ao objeto de dados, o parâmetro szName ou pId deverá ser não **nulo**.</span><span class="sxs-lookup"><span data-stu-id="46ee4-132">If a data reference object will reference the data object, either the szName or pId parameter must be non-**NULL**.</span></span>

<span data-ttu-id="46ee4-133">Salve os dados criados no disco usando o método [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) .</span><span class="sxs-lookup"><span data-stu-id="46ee4-133">Save the created data to disk by using the [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ee4-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46ee4-134">Requirements</span></span>



| <span data-ttu-id="46ee4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="46ee4-135">Requirement</span></span> | <span data-ttu-id="46ee4-136">Valor</span><span class="sxs-lookup"><span data-stu-id="46ee4-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46ee4-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46ee4-137">Header</span></span><br/>  | <dl> <span data-ttu-id="46ee4-138"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="46ee4-138"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="46ee4-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46ee4-139">Library</span></span><br/> | <dl> <span data-ttu-id="46ee4-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46ee4-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="46ee4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="46ee4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ee4-142">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="46ee4-142">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
