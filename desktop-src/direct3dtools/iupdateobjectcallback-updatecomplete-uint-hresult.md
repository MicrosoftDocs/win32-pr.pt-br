---
description: Um retorno de chamada usado para notificar o host de que um objeto foi atualizado.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IUpdateObjectCallback:: UpdateComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087664"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span data-ttu-id="2767d-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>Método IUpdateObjectCallback:: UpdateComplete</span><span class="sxs-lookup"><span data-stu-id="2767d-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete method</span></span>

<span data-ttu-id="2767d-104">Um retorno de chamada usado para notificar o host de que um objeto foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="2767d-104">A callback used to notify the host that an object was updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2767d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2767d-105">Syntax</span></span>


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a><span data-ttu-id="2767d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2767d-106">Parameters</span></span>

<span data-ttu-id="2767d-107">*objectaddress* </span><span class="sxs-lookup"><span data-stu-id="2767d-107">*objectAddress* </span></span>  
<span data-ttu-id="2767d-108">A ID do objeto que foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="2767d-108">The ID of the object that was updated.</span></span>

<span data-ttu-id="2767d-109">*disso* </span><span class="sxs-lookup"><span data-stu-id="2767d-109">*result* </span></span>  
<span data-ttu-id="2767d-110">Indica se a atualização foi bem-sucedida ou não.</span><span class="sxs-lookup"><span data-stu-id="2767d-110">Indicates whether or not the update succeeded.</span></span>

## <a name="return-value"></a><span data-ttu-id="2767d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2767d-111">Return value</span></span>

<span data-ttu-id="2767d-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2767d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2767d-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2767d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2767d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2767d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2767d-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2767d-115">Header</span></span></p></td><td><span data-ttu-id="2767d-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2767d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2767d-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="2767d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2767d-118">**IUpdateObjectCallback**</span><span class="sxs-lookup"><span data-stu-id="2767d-118">**IUpdateObjectCallback**</span></span>](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
