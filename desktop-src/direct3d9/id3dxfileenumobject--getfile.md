---
description: Recupera o objeto ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'Método ID3DXFileEnumObject:: GetFile (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930650"
---
# <a name="id3dxfileenumobjectgetfile-method"></a><span data-ttu-id="180f4-103">Método ID3DXFileEnumObject:: GetFile</span><span class="sxs-lookup"><span data-stu-id="180f4-103">ID3DXFileEnumObject::GetFile method</span></span>

<span data-ttu-id="180f4-104">Recupera o objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="180f4-104">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="180f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="180f4-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="180f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="180f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180f4-107">*ppFile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="180f4-107">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="180f4-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="180f4-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="180f4-109">Endereço de um ponteiro para uma interface [**ID3DXFile**](id3dxfile.md) , que representa o objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="180f4-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the returned object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="180f4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="180f4-110">Return value</span></span>

<span data-ttu-id="180f4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="180f4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="180f4-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="180f4-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="180f4-113">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="180f4-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="180f4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="180f4-114">Requirements</span></span>



| <span data-ttu-id="180f4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="180f4-115">Requirement</span></span> | <span data-ttu-id="180f4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="180f4-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="180f4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="180f4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="180f4-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="180f4-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="180f4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="180f4-119">Library</span></span><br/> | <dl> <span data-ttu-id="180f4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="180f4-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="180f4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="180f4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180f4-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="180f4-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 




