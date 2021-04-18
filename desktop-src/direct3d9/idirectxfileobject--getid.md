---
description: Recupera um ponteiro para o GUID que identifica um objeto de arquivo do DirectX. Preterido.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'Método IDirectXFileObject:: GetId (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762062"
---
# <a name="idirectxfileobjectgetid-method"></a><span data-ttu-id="3b1fe-104">Método IDirectXFileObject:: GetId</span><span class="sxs-lookup"><span data-stu-id="3b1fe-104">IDirectXFileObject::GetId method</span></span>

<span data-ttu-id="3b1fe-105">Recupera um ponteiro para o GUID que identifica um objeto de arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="3b1fe-105">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="3b1fe-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3b1fe-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b1fe-107">Syntax</span></span>


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="3b1fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b1fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1fe-109">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3b1fe-109">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1fe-110">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="3b1fe-110">Type: **LPGUID**</span></span>

<span data-ttu-id="3b1fe-111">Ponteiro para um GUID para receber a ID do objeto.</span><span class="sxs-lookup"><span data-stu-id="3b1fe-111">Pointer to a GUID to receive the object's ID.</span></span> <span data-ttu-id="3b1fe-112">A função definirá o GUID como um GUID **nulo** se o objeto não tiver uma ID.</span><span class="sxs-lookup"><span data-stu-id="3b1fe-112">The function will set the GUID to a **NULL** GUID if the object does not have an ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1fe-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b1fe-113">Return value</span></span>

<span data-ttu-id="3b1fe-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b1fe-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b1fe-115">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3b1fe-115">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3b1fe-116">Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="3b1fe-116">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b1fe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b1fe-117">Requirements</span></span>



| <span data-ttu-id="3b1fe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b1fe-118">Requirement</span></span> | <span data-ttu-id="3b1fe-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3b1fe-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1fe-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b1fe-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3b1fe-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b1fe-121"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b1fe-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b1fe-122">Library</span></span><br/> | <dl> <span data-ttu-id="3b1fe-123"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b1fe-123"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b1fe-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b1fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1fe-125">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="3b1fe-125">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 




