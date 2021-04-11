---
description: Solicitações para obter o conteúdo bruto de um bloco.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ITileRequest:: RequestBufferTileAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163872"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span data-ttu-id="ec87c-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>Método ITileRequest:: RequestBufferTileAsync</span><span class="sxs-lookup"><span data-stu-id="ec87c-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest::RequestBufferTileAsync method</span></span>

<span data-ttu-id="ec87c-104">Solicitações para obter o conteúdo bruto de um bloco.</span><span class="sxs-lookup"><span data-stu-id="ec87c-104">Requests to get the raw contents of a tile.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec87c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec87c-105">Syntax</span></span>


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ec87c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec87c-106">Parameters</span></span>

<span data-ttu-id="ec87c-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="ec87c-107">*eventID* </span></span>  
<span data-ttu-id="ec87c-108">O evento especificado para corresponder o conteúdo do bloco a (por exemplo, um destino de renderização pode mudar ao longo do tempo).</span><span class="sxs-lookup"><span data-stu-id="ec87c-108">The specified event to match the tile's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="ec87c-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="ec87c-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="ec87c-110">O endereço do bloco especificado.</span><span class="sxs-lookup"><span data-stu-id="ec87c-110">The address of the specified tile.</span></span>

<span data-ttu-id="ec87c-111">*Grupo* </span><span class="sxs-lookup"><span data-stu-id="ec87c-111">*File* </span></span>  
<span data-ttu-id="ec87c-112">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde os resultados são gravados.</span><span class="sxs-lookup"><span data-stu-id="ec87c-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="ec87c-113">*tileIndex* </span><span class="sxs-lookup"><span data-stu-id="ec87c-113">*tileIndex* </span></span>  
<span data-ttu-id="ec87c-114">O índice do bloco especificado.</span><span class="sxs-lookup"><span data-stu-id="ec87c-114">The index of the specified tile.</span></span>

<span data-ttu-id="ec87c-115">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ec87c-115">*requestCallback* </span></span>  
<span data-ttu-id="ec87c-116">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="ec87c-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ec87c-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ec87c-117">*requestCookie* </span></span>  
<span data-ttu-id="ec87c-118">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="ec87c-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ec87c-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ec87c-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ec87c-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ec87c-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec87c-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec87c-121">Return value</span></span>

<span data-ttu-id="ec87c-122">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="ec87c-122">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="ec87c-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec87c-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec87c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec87c-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ec87c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec87c-125">Header</span></span></p></td><td><span data-ttu-id="ec87c-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ec87c-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ec87c-127"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="ec87c-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ec87c-128">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="ec87c-128">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
