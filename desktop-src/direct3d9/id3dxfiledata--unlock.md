---
description: 'Termina o ciclo de vida do ponteiro ppData retornado por ID3DXFileData:: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'Método ID3DXFileData:: Unlock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664036"
---
# <a name="id3dxfiledataunlock-method"></a><span data-ttu-id="450b1-103">Método ID3DXFileData:: Unlock</span><span class="sxs-lookup"><span data-stu-id="450b1-103">ID3DXFileData::Unlock method</span></span>

<span data-ttu-id="450b1-104">Termina o ciclo de vida do ponteiro *ppData* retornado por [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="450b1-104">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="450b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="450b1-105">Syntax</span></span>


```C++
BOOL Unlock();
```



## <a name="parameters"></a><span data-ttu-id="450b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="450b1-106">Parameters</span></span>

<span data-ttu-id="450b1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="450b1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="450b1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="450b1-108">Return value</span></span>

<span data-ttu-id="450b1-109">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="450b1-109">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="450b1-110">O valor de retorno é S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="450b1-110">The return value is S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="450b1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="450b1-111">Remarks</span></span>

<span data-ttu-id="450b1-112">Você deve garantir que o número de chamadas [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) corresponda ao número de chamadas **ID3DXFileData:: Unlock** .</span><span class="sxs-lookup"><span data-stu-id="450b1-112">You must ensure that the number of [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) calls matches the number of **ID3DXFileData::Unlock** calls.</span></span> <span data-ttu-id="450b1-113">Depois de chamar Unlock, o ponteiro ppData retornado por **ID3DXFileData:: Lock** não deve mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="450b1-113">After calling Unlock, the ppData pointer returned by **ID3DXFileData::Lock** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="450b1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="450b1-114">Requirements</span></span>



| <span data-ttu-id="450b1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="450b1-115">Requirement</span></span> | <span data-ttu-id="450b1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="450b1-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="450b1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="450b1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="450b1-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="450b1-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="450b1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="450b1-119">Library</span></span><br/> | <dl> <span data-ttu-id="450b1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="450b1-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="450b1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="450b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450b1-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="450b1-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
