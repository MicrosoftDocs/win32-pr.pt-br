---
description: Recupera o GUID do modelo do objeto. Preterido.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'Método IDirectXFileData:: GetType (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091985"
---
# <a name="idirectxfiledatagettype-method"></a><span data-ttu-id="3a182-104">Método IDirectXFileData:: GetType</span><span class="sxs-lookup"><span data-stu-id="3a182-104">IDirectXFileData::GetType method</span></span>

<span data-ttu-id="3a182-105">Recupera o GUID do modelo do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a182-105">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="3a182-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3a182-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a182-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a182-107">Syntax</span></span>


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a><span data-ttu-id="3a182-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a182-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a182-109">*ppguid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3a182-109">*ppguid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3a182-110">Tipo: **[**GUID**](guid.md) \* \* const**</span><span class="sxs-lookup"><span data-stu-id="3a182-110">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="3a182-111">Endereço de um ponteiro para receber o GUID do modelo do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a182-111">Address of a pointer to receive the GUID of the object's template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a182-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a182-112">Return value</span></span>

<span data-ttu-id="3a182-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a182-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a182-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a182-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3a182-115">Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="3a182-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a182-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a182-116">Requirements</span></span>



| <span data-ttu-id="3a182-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a182-117">Requirement</span></span> | <span data-ttu-id="3a182-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3a182-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a182-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a182-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3a182-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a182-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a182-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a182-121">Library</span></span><br/> | <dl> <span data-ttu-id="3a182-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a182-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a182-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a182-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a182-124">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="3a182-124">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 




