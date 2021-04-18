---
description: Recupera o objeto de dados que tem o nome especificado.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'Método ID3DXFileEnumObject:: GetDataObjectByName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786203"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="257e7-103">Método ID3DXFileEnumObject:: GetDataObjectByName</span><span class="sxs-lookup"><span data-stu-id="257e7-103">ID3DXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="257e7-104">Recupera o objeto de dados que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="257e7-104">Retrieves the data object that has the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="257e7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="257e7-105">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="257e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="257e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="257e7-107">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="257e7-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="257e7-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="257e7-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="257e7-109">Ponteiro para o nome solicitado.</span><span class="sxs-lookup"><span data-stu-id="257e7-109">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="257e7-110">*ppObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="257e7-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="257e7-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="257e7-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="257e7-112">Endereço de um ponteiro para uma interface [**ID3DXFileData**](id3dxfiledata.md) , que representa o objeto de dados de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="257e7-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="257e7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="257e7-113">Return value</span></span>

<span data-ttu-id="257e7-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="257e7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="257e7-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="257e7-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="257e7-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADVALUE, DXFILEERR não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="257e7-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="257e7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="257e7-117">Remarks</span></span>

<span data-ttu-id="257e7-118">Obtenha o nome szName do objeto de dados do arquivo atual com o método [**ID3DXFileData:: GetName**](id3dxfiledata--getname.md) .</span><span class="sxs-lookup"><span data-stu-id="257e7-118">Obtain the name szName of the current file data object with the [**ID3DXFileData::GetName**](id3dxfiledata--getname.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="257e7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="257e7-119">Requirements</span></span>



| <span data-ttu-id="257e7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="257e7-120">Requirement</span></span> | <span data-ttu-id="257e7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="257e7-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="257e7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="257e7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="257e7-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="257e7-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="257e7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="257e7-124">Library</span></span><br/> | <dl> <span data-ttu-id="257e7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="257e7-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="257e7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="257e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257e7-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="257e7-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
