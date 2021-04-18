---
description: Recupera o objeto de enumeração neste objeto de dados de arquivo.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'Método ID3DXFileData:: getenum (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798526"
---
# <a name="id3dxfiledatagetenum-method"></a><span data-ttu-id="5aff5-103">Método ID3DXFileData:: getenum</span><span class="sxs-lookup"><span data-stu-id="5aff5-103">ID3DXFileData::GetEnum method</span></span>

<span data-ttu-id="5aff5-104">Recupera o objeto de enumeração neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5aff5-104">Retrieves the enumeration object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aff5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5aff5-105">Syntax</span></span>


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="5aff5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5aff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aff5-107">*ppObj* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5aff5-107">*ppObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aff5-108">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5aff5-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="5aff5-109">Endereço de um ponteiro para receber o objeto de enumeração neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5aff5-109">Address of a pointer to receive the enumeration object in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aff5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5aff5-110">Return value</span></span>

<span data-ttu-id="5aff5-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5aff5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5aff5-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5aff5-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5aff5-113">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="5aff5-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aff5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aff5-114">Requirements</span></span>



| <span data-ttu-id="5aff5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aff5-115">Requirement</span></span> | <span data-ttu-id="5aff5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5aff5-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5aff5-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5aff5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5aff5-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aff5-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="5aff5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5aff5-119">Library</span></span><br/> | <dl> <span data-ttu-id="5aff5-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aff5-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5aff5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5aff5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aff5-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="5aff5-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




