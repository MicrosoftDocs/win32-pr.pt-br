---
description: Recupera um ponteiro para este nó de dados do arquivo ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'Método ID3DXFileSaveData:: getsave (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173179"
---
# <a name="id3dxfilesavedatagetsave-method"></a><span data-ttu-id="65429-103">Método ID3DXFileSaveData:: getsave</span><span class="sxs-lookup"><span data-stu-id="65429-103">ID3DXFileSaveData::GetSave method</span></span>

<span data-ttu-id="65429-104">Recupera um ponteiro para este nó de dados do arquivo [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="65429-104">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="65429-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65429-105">Syntax</span></span>


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="65429-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65429-107">*ppObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="65429-107">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65429-108">Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="65429-108">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="65429-109">Endereço de um ponteiro para uma interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) que representa esse nó de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="65429-109">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface representing this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65429-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65429-110">Return value</span></span>

<span data-ttu-id="65429-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65429-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65429-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65429-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="65429-113">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="65429-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="65429-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65429-114">Requirements</span></span>



| <span data-ttu-id="65429-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="65429-115">Requirement</span></span> | <span data-ttu-id="65429-116">Valor</span><span class="sxs-lookup"><span data-stu-id="65429-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65429-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65429-117">Header</span></span><br/>  | <dl> <span data-ttu-id="65429-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="65429-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="65429-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65429-119">Library</span></span><br/> | <dl> <span data-ttu-id="65429-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65429-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="65429-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="65429-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65429-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="65429-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




