---
description: Um retorno de chamada que notifica o host de informações de buffer genéricas retornadas pela solicitação assocaited.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IGenericBufferDataCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646062"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span data-ttu-id="4747f-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>Método IGenericBufferDataCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="4747f-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback method</span></span>

<span data-ttu-id="4747f-104">Um retorno de chamada que notifica o host de informações de buffer genéricas retornadas pela solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="4747f-104">A callback that notifies the host of generic buffer information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="4747f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4747f-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a><span data-ttu-id="4747f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4747f-106">Parameters</span></span>

<span data-ttu-id="4747f-107">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="4747f-107">*size* </span></span>  
<span data-ttu-id="4747f-108">O tamanho do conteúdo do buffer em bytes.</span><span class="sxs-lookup"><span data-stu-id="4747f-108">The size of the buffer contents in bytes.</span></span>

<span data-ttu-id="4747f-109">*\_buffer count0* </span><span class="sxs-lookup"><span data-stu-id="4747f-109">*count0\_buffer* </span></span>  
<span data-ttu-id="4747f-110">O conteúdo do buffer.</span><span class="sxs-lookup"><span data-stu-id="4747f-110">The buffer contents.</span></span> <span data-ttu-id="4747f-111">Na maioria dos casos, esses são dados XML.</span><span class="sxs-lookup"><span data-stu-id="4747f-111">In most cases this is XML data.</span></span>

<span data-ttu-id="4747f-112">*Escreva* </span><span class="sxs-lookup"><span data-stu-id="4747f-112">*type* </span></span>  
<span data-ttu-id="4747f-113">Uma cadeia de caracteres COM que indica o tipo de conteúdo retornado no buffer.</span><span class="sxs-lookup"><span data-stu-id="4747f-113">A COM string that indicates the type of content returned in the buffer.</span></span>

## <a name="return-value"></a><span data-ttu-id="4747f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4747f-114">Return value</span></span>

<span data-ttu-id="4747f-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4747f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4747f-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4747f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4747f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4747f-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4747f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4747f-118">Header</span></span></p></td><td><span data-ttu-id="4747f-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4747f-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4747f-120"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="4747f-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4747f-121">**IGenericBufferDataCallback**</span><span class="sxs-lookup"><span data-stu-id="4747f-121">**IGenericBufferDataCallback**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
