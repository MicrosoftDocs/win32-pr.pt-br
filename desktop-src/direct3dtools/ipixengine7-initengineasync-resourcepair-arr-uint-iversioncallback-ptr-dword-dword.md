---
description: O passa os recursos de forma assíncrona para o mecanismo, como cadeias de caracteres para mensagens de erro.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine7:: InitEngineAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 21d98a207b0194f281abc2800cd63f9be7de5073
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456852"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span data-ttu-id="b4fe9-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>Método IPixEngine7:: InitEngineAsync</span><span class="sxs-lookup"><span data-stu-id="b4fe9-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7::InitEngineAsync method</span></span>

<span data-ttu-id="b4fe9-104">O passa os recursos de forma assíncrona para o mecanismo, como cadeias de caracteres para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="b4fe9-104">Asynchronously passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fe9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4fe9-105">Syntax</span></span>


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b4fe9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4fe9-106">Parameters</span></span>

<span data-ttu-id="b4fe9-107">*recursos do count1 \_* </span><span class="sxs-lookup"><span data-stu-id="b4fe9-107">*count1\_resources* </span></span>  
<span data-ttu-id="b4fe9-108">Uma matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4fe9-108">An array of resources.</span></span>

<span data-ttu-id="b4fe9-109">*contar* </span><span class="sxs-lookup"><span data-stu-id="b4fe9-109">*count* </span></span>  
<span data-ttu-id="b4fe9-110">O número de recursos em \_ recursos count1</span><span class="sxs-lookup"><span data-stu-id="b4fe9-110">The number of resources in count1\_resources</span></span>

<span data-ttu-id="b4fe9-111">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="b4fe9-111">*versionCallback* </span></span>  
<span data-ttu-id="b4fe9-112">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="b4fe9-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b4fe9-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b4fe9-113">*requestCookie* </span></span>  
<span data-ttu-id="b4fe9-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="b4fe9-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b4fe9-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b4fe9-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b4fe9-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b4fe9-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4fe9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4fe9-117">Return value</span></span>

<span data-ttu-id="b4fe9-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b4fe9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4fe9-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4fe9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4fe9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4fe9-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b4fe9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4fe9-121">Header</span></span></p></td><td><span data-ttu-id="b4fe9-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b4fe9-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b4fe9-123"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="b4fe9-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b4fe9-124">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="b4fe9-124">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
