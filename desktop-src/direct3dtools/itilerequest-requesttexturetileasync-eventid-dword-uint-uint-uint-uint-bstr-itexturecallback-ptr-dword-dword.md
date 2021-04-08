---
description: Solicitações para obter o conteúdo de uma textura com um lado do ladrilho como um. Arquivo DDS (superfície do DirectDraw).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ITileRequest:: RequestTextureTileAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087669"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span data-ttu-id="a9c4b-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>Método ITileRequest:: RequestTextureTileAsync</span><span class="sxs-lookup"><span data-stu-id="a9c4b-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync method</span></span>

<span data-ttu-id="a9c4b-104">Solicitações para obter o conteúdo de uma textura com um lado do ladrilho como um. Arquivo DDS (superfície do DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="a9c4b-104">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9c4b-105">Syntax</span></span>


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="a9c4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9c4b-106">Parameters</span></span>

<span data-ttu-id="a9c4b-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-107">*eventID* </span></span>  
<span data-ttu-id="a9c4b-108">O evento especificado para corresponder ao conteúdo do buffer (por exemplo, um destino de renderização pode mudar ao longo do tempo).</span><span class="sxs-lookup"><span data-stu-id="a9c4b-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="a9c4b-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-109">*textureFileptr* </span></span>  
<span data-ttu-id="a9c4b-110">O endereço do objeto de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-110">The address of the specified texture object.</span></span>

<span data-ttu-id="a9c4b-111">*tileSubresource* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-111">*tileSubresource* </span></span>  
<span data-ttu-id="a9c4b-112">O subrecurso especificado do bloco.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-112">The specified subresource of the tile.</span></span>

<span data-ttu-id="a9c4b-113">*tileX* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-113">*tileX* </span></span>  
<span data-ttu-id="a9c4b-114">A posição X do bloco especificado.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-114">The specified tile X position.</span></span>

<span data-ttu-id="a9c4b-115">*bloco* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-115">*tileY* </span></span>  
<span data-ttu-id="a9c4b-116">A posição Y do bloco especificado.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-116">The specified tile Y position.</span></span>

<span data-ttu-id="a9c4b-117">*tileZ* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-117">*tileZ* </span></span>  
<span data-ttu-id="a9c4b-118">A posição Z do bloco especificado.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-118">The specified tile Z position.</span></span>

<span data-ttu-id="a9c4b-119">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-119">*ddsFilename* </span></span>  
<span data-ttu-id="a9c4b-120">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo. DDS onde os resultados são gravados.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-120">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="a9c4b-121">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-121">*pRequestCallback* </span></span>  
<span data-ttu-id="a9c4b-122">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-122">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="a9c4b-123">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-123">*requestCookie* </span></span>  
<span data-ttu-id="a9c4b-124">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-124">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="a9c4b-125">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="a9c4b-125">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="a9c4b-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-126">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9c4b-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9c4b-127">Return value</span></span>

<span data-ttu-id="a9c4b-128">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9c4b-129">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9c4b-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c4b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9c4b-130">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a9c4b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9c4b-131">Header</span></span></p></td><td><span data-ttu-id="a9c4b-132">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a9c4b-132">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a9c4b-133"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="a9c4b-133"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a9c4b-134">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="a9c4b-134">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
