---
description: Solicitações para obter o conteúdo de uma textura como um. Arquivo DDS (superfície do DirectDraw).
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ITextureRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456836"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span data-ttu-id="a7da0-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>Método ITextureRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="a7da0-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest::RequestAsync method</span></span>

<span data-ttu-id="a7da0-104">Solicitações para obter o conteúdo de uma textura como um. Arquivo DDS (superfície do DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="a7da0-104">Requests to get the contents of a texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7da0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7da0-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="a7da0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7da0-106">Parameters</span></span>

<span data-ttu-id="a7da0-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="a7da0-107">*eventID* </span></span>  
<span data-ttu-id="a7da0-108">O evento especificado para corresponder ao conteúdo do buffer (por exemplo, um destino de renderização pode mudar ao longo do tempo).</span><span class="sxs-lookup"><span data-stu-id="a7da0-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="a7da0-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="a7da0-109">*textureFileptr* </span></span>  
<span data-ttu-id="a7da0-110">O endereço do objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a7da0-110">The address of the texture object.</span></span>

<span data-ttu-id="a7da0-111">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="a7da0-111">*ddsFilename* </span></span>  
<span data-ttu-id="a7da0-112">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo. DDS onde os resultados são gravados.</span><span class="sxs-lookup"><span data-stu-id="a7da0-112">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="a7da0-113">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="a7da0-113">*pRequestCallback* </span></span>  
<span data-ttu-id="a7da0-114">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="a7da0-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="a7da0-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="a7da0-115">*requestCookie* </span></span>  
<span data-ttu-id="a7da0-116">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="a7da0-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="a7da0-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="a7da0-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="a7da0-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="a7da0-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7da0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7da0-119">Return value</span></span>

<span data-ttu-id="a7da0-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a7da0-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7da0-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7da0-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7da0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7da0-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a7da0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7da0-123">Header</span></span></p></td><td><span data-ttu-id="a7da0-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a7da0-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a7da0-125"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="a7da0-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a7da0-126">**ITextureRequest**</span><span class="sxs-lookup"><span data-stu-id="a7da0-126">**ITextureRequest**</span></span>](/windows/desktop/direct3dtools/itexturerequest)

 

 
