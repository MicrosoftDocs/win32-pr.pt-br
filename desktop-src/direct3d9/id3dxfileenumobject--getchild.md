---
description: 'Método ID3DXFileEnumObject:: GetChild – recupera um objeto filho neste objeto de dados de arquivo.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'Método ID3DXFileEnumObject:: GetChild (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090354"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="5d239-103">Método ID3DXFileEnumObject:: GetChild</span><span class="sxs-lookup"><span data-stu-id="5d239-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="5d239-104">Recupera um objeto filho neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d239-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d239-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d239-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="5d239-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d239-107">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5d239-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d239-108">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d239-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d239-109">ID do objeto filho a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="5d239-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5d239-110">*ppObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5d239-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d239-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d239-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="5d239-112">Endereço de um ponteiro para receber o ponteiro de interface do objeto filho.</span><span class="sxs-lookup"><span data-stu-id="5d239-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d239-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5d239-113">Return value</span></span>

<span data-ttu-id="5d239-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d239-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d239-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5d239-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5d239-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="5d239-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d239-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d239-117">Requirements</span></span>



| <span data-ttu-id="5d239-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d239-118">Requirement</span></span> | <span data-ttu-id="5d239-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5d239-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d239-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d239-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5d239-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d239-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="5d239-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d239-122">Library</span></span><br/> | <dl> <span data-ttu-id="5d239-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d239-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5d239-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5d239-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d239-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="5d239-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
