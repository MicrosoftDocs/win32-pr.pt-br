---
description: Cria um objeto enumerador que lerá um arquivo. x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'Método ID3DXFile:: createenumobject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790312"
---
# <a name="id3dxfilecreateenumobject-method"></a><span data-ttu-id="3f296-103">Método ID3DXFile:: createenumobject</span><span class="sxs-lookup"><span data-stu-id="3f296-103">ID3DXFile::CreateEnumObject method</span></span>

<span data-ttu-id="3f296-104">Cria um objeto enumerador que lerá um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="3f296-104">Creates an enumerator object that will read a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f296-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f296-105">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="3f296-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f296-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f296-107">*pvSource* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f296-107">*pvSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f296-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f296-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f296-109">A fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="3f296-109">The data source.</span></span> <span data-ttu-id="3f296-110">Ou:</span><span class="sxs-lookup"><span data-stu-id="3f296-110">Either:</span></span>

-   <span data-ttu-id="3f296-111">Um nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="3f296-111">A file name</span></span>
-   <span data-ttu-id="3f296-112">Uma estrutura [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)</span><span class="sxs-lookup"><span data-stu-id="3f296-112">A [**D3DXF\_FILELOADMEMORY**](d3dxf-fileloadmemory.md) structure</span></span>
-   <span data-ttu-id="3f296-113">Uma estrutura [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)</span><span class="sxs-lookup"><span data-stu-id="3f296-113">A [**D3DXF\_FILELOADRESOURCE**](d3dxf-fileloadresource.md) structure</span></span>

<span data-ttu-id="3f296-114">Dependendo do valor de LoadFlags.</span><span class="sxs-lookup"><span data-stu-id="3f296-114">Depending on the value of loadflags.</span></span>

</dd> <dt>

<span data-ttu-id="3f296-115">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="3f296-115">*loadflags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f296-116">Tipo: **[D3DXF \_ fileloadoptions](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="3f296-116">Type: **[D3DXF\_FILELOADOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="3f296-117">Valor que especifica a origem dos dados.</span><span class="sxs-lookup"><span data-stu-id="3f296-117">Value that specifies the source of the data.</span></span> <span data-ttu-id="3f296-118">Esse valor pode ser um dos sinalizadores [D3DXF \_ fileloadoptions](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="3f296-118">This value can be one of the [D3DXF\_FILELOADOPTIONS](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="3f296-119">*ppEnumObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f296-119">*ppEnumObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f296-120">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3f296-120">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="3f296-121">Endereço de um ponteiro para uma interface [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , que representa o objeto enumerador criado.</span><span class="sxs-lookup"><span data-stu-id="3f296-121">Address of a pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f296-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f296-122">Return value</span></span>

<span data-ttu-id="3f296-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f296-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f296-124">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f296-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3f296-125">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="3f296-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f296-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f296-126">Remarks</span></span>

<span data-ttu-id="3f296-127">Depois de usar esse método, use um dos métodos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) para recuperar um objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="3f296-127">After using this method, use one of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f296-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f296-128">Requirements</span></span>



| <span data-ttu-id="3f296-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f296-129">Requirement</span></span> | <span data-ttu-id="3f296-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3f296-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f296-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f296-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3f296-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f296-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="3f296-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f296-133">Library</span></span><br/> | <dl> <span data-ttu-id="3f296-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f296-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3f296-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f296-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f296-136">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="3f296-136">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="3f296-137">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="3f296-137">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
