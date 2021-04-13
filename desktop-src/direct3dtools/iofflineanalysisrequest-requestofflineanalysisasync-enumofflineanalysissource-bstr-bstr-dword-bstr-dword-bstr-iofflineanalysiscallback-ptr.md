---
description: Solicitações para executar análise offline com a origem, o manifesto, os parâmetros e o quadro especificado especificados.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IOfflineAnalysisRequest:: RequestOfflineAnalysisAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d027b9ec463c0bebfefca3ee7f9af4b50c514755
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370233"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span data-ttu-id="c4bb1-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Método IOfflineAnalysisRequest:: RequestOfflineAnalysisAsync</span><span class="sxs-lookup"><span data-stu-id="c4bb1-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync method</span></span>

<span data-ttu-id="c4bb1-104">Solicitações para executar análise offline com a origem, o manifesto, os parâmetros e o quadro especificado especificados.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-104">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bb1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4bb1-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="c4bb1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4bb1-106">Parameters</span></span>

<span data-ttu-id="c4bb1-107">*análise* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-107">*analysisSource* </span></span>  
<span data-ttu-id="c4bb1-108">Especifica em que a origem da análise é proveniente dos relatórios armazenados em cache ou da reprodução.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-108">Specfies where the analysis source come from cached reports or from playback.</span></span>

<span data-ttu-id="c4bb1-109">*manifestXml* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-109">*manifestXml* </span></span>  
<span data-ttu-id="c4bb1-110">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo de manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-110">A COM string containing the pathname of the XML manifest file.</span></span>

<span data-ttu-id="c4bb1-111">*parametersXml* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-111">*parametersXml* </span></span>  
<span data-ttu-id="c4bb1-112">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo de parâmetros XML.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-112">A COM string containing the pathname of the XML parameters file.</span></span>

<span data-ttu-id="c4bb1-113">*cookie* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-113">*cookie* </span></span>  
<span data-ttu-id="c4bb1-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c4bb1-115">*captureFullFileName* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-115">*captureFullFileName* </span></span>  
<span data-ttu-id="c4bb1-116">Uma cadeia de caracteres COM que contém o nome de caminho absoluto do arquivo de captura (. vsglog).</span><span class="sxs-lookup"><span data-stu-id="c4bb1-116">A COM string containing the absolute pathname of the capture file (.vsglog).</span></span>

<span data-ttu-id="c4bb1-117">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-117">*frameNumber* </span></span>  
<span data-ttu-id="c4bb1-118">O quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-118">The specified frame.</span></span>

<span data-ttu-id="c4bb1-119">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-119">*outputFullFileName* </span></span>  
<span data-ttu-id="c4bb1-120">Uma cadeia de caracteres COM que contém o nome de caminho absoluto do arquivo em que a saída é gravada.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-120">A COM string containing the absolute pathname of the file where output is written.</span></span>

<span data-ttu-id="c4bb1-121">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="c4bb1-121">*requestCallback* </span></span>  
<span data-ttu-id="c4bb1-122">O endereço de um retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-122">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4bb1-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4bb1-123">Return value</span></span>

<span data-ttu-id="c4bb1-124">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4bb1-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4bb1-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4bb1-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4bb1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4bb1-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c4bb1-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4bb1-127">Header</span></span></p></td><td><span data-ttu-id="c4bb1-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c4bb1-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c4bb1-129"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="c4bb1-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c4bb1-130">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="c4bb1-130">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
