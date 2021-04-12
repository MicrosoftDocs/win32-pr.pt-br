---
description: Obtém a interface ID3DXFile do objeto que criou este objeto ID3DXFileSaveObject.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'Método ID3DXFileSaveObject:: GetFile (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370978"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a><span data-ttu-id="e1633-103">Método ID3DXFileSaveObject:: GetFile</span><span class="sxs-lookup"><span data-stu-id="e1633-103">ID3DXFileSaveObject::GetFile method</span></span>

<span data-ttu-id="e1633-104">Obtém a interface [**ID3DXFile**](id3dxfile.md) do objeto que criou este objeto [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="e1633-104">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1633-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1633-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="e1633-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1633-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1633-107">*ppFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1633-107">*ppFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1633-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="e1633-108">Type: **[**ID3DXFile**](id3dxfile.md)**</span></span>

<span data-ttu-id="e1633-109">Endereço de um ponteiro para um objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e1633-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1633-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1633-110">Return value</span></span>

<span data-ttu-id="e1633-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1633-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1633-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1633-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e1633-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, e \_ nointerface, e \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e1633-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, E\_NOINTERFACE, E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1633-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1633-114">Requirements</span></span>



| <span data-ttu-id="e1633-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1633-115">Requirement</span></span> | <span data-ttu-id="e1633-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e1633-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1633-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1633-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e1633-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1633-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e1633-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1633-119">Library</span></span><br/> | <dl> <span data-ttu-id="e1633-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1633-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e1633-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1633-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1633-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="e1633-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




