---
description: Recupera o GUID deste nó de dados do arquivo ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'Método ID3DXFileSaveData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781401"
---
# <a name="id3dxfilesavedatagetid-method"></a><span data-ttu-id="e43b5-103">Método ID3DXFileSaveData:: GetId</span><span class="sxs-lookup"><span data-stu-id="e43b5-103">ID3DXFileSaveData::GetId method</span></span>

<span data-ttu-id="e43b5-104">Recupera o GUID deste nó de dados do arquivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="e43b5-104">Retrieves the GUID of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e43b5-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="e43b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e43b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43b5-107">*pid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e43b5-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43b5-108">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="e43b5-108">Type: **LPGUID**</span></span>

<span data-ttu-id="e43b5-109">Ponteiro para um GUID para receber a ID deste nó de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e43b5-109">Pointer to a GUID to receive the ID of this file data node.</span></span> <span data-ttu-id="e43b5-110">Se o objeto não tiver nenhuma ID, o valor do parâmetro retornado será GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="e43b5-110">If the object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43b5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e43b5-111">Return value</span></span>

<span data-ttu-id="e43b5-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e43b5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e43b5-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e43b5-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e43b5-114">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e43b5-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e43b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e43b5-115">Requirements</span></span>



| <span data-ttu-id="e43b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e43b5-116">Requirement</span></span> | <span data-ttu-id="e43b5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e43b5-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e43b5-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e43b5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e43b5-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e43b5-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e43b5-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e43b5-120">Library</span></span><br/> | <dl> <span data-ttu-id="e43b5-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e43b5-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e43b5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e43b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43b5-123">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="e43b5-123">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




