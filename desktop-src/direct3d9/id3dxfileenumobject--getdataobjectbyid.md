---
description: Recupera o objeto de dados que tem o GUID especificado.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'Método ID3DXFileEnumObject:: GetDataObjectById (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788712"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="80e11-103">Método ID3DXFileEnumObject:: GetDataObjectById</span><span class="sxs-lookup"><span data-stu-id="80e11-103">ID3DXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="80e11-104">Recupera o objeto de dados que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="80e11-104">Retrieves the data object that has the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e11-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80e11-105">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="80e11-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80e11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e11-107">*rguid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80e11-107">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e11-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="80e11-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="80e11-109">Referência ao GUID solicitado.</span><span class="sxs-lookup"><span data-stu-id="80e11-109">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="80e11-110">*ppDataObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="80e11-110">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80e11-111">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="80e11-111">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)\***</span></span>

<span data-ttu-id="80e11-112">Endereço de um ponteiro para uma interface [**ID3DXFileData**](id3dxfiledata.md) , que representa o objeto de dados de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="80e11-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e11-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80e11-113">Return value</span></span>

<span data-ttu-id="80e11-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80e11-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80e11-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80e11-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="80e11-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADVALUE, DXFILEERR não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="80e11-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="80e11-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="80e11-117">Remarks</span></span>

<span data-ttu-id="80e11-118">Obtenha o rguid do GUID do objeto de dados do arquivo atual com o método [**ID3DXFileData:: GetID**](id3dxfiledata--getid.md) .</span><span class="sxs-lookup"><span data-stu-id="80e11-118">Obtain the GUID rguid of the current file data object with the [**ID3DXFileData::GetId**](id3dxfiledata--getid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e11-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80e11-119">Requirements</span></span>



| <span data-ttu-id="80e11-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e11-120">Requirement</span></span> | <span data-ttu-id="80e11-121">Valor</span><span class="sxs-lookup"><span data-stu-id="80e11-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80e11-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80e11-122">Header</span></span><br/>  | <dl> <span data-ttu-id="80e11-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="80e11-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="80e11-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80e11-124">Library</span></span><br/> | <dl> <span data-ttu-id="80e11-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80e11-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="80e11-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="80e11-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e11-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="80e11-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
