---
description: Uma função de retorno de chamada usada para notificar o host que a análise offline foi concluída.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IOfflineAnalysisCallback:: OfflineAnalysisComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500721"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span data-ttu-id="d3481-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>Método IOfflineAnalysisCallback:: OfflineAnalysisComplete</span><span class="sxs-lookup"><span data-stu-id="d3481-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete method</span></span>

<span data-ttu-id="d3481-104">Uma função de retorno de chamada usada para notificar o host que a análise offline foi concluída.</span><span class="sxs-lookup"><span data-stu-id="d3481-104">A callback function used to notify the host that offline analysis has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3481-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3481-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="d3481-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3481-106">Parameters</span></span>

<span data-ttu-id="d3481-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="d3481-107">*cookie* </span></span>  
<span data-ttu-id="d3481-108">Um cookie que identifica exclusivamente a solicitação que iniciou a análise offline.</span><span class="sxs-lookup"><span data-stu-id="d3481-108">A cookie that uniquely identifies the request which initiated offline analysis.</span></span>

<span data-ttu-id="d3481-109">*disso* </span><span class="sxs-lookup"><span data-stu-id="d3481-109">*result* </span></span>  
<span data-ttu-id="d3481-110">Indica se a análise offline foi bem-sucedida ou falhou.</span><span class="sxs-lookup"><span data-stu-id="d3481-110">Indicates whether offline analysis succeeded or failed.</span></span> <span data-ttu-id="d3481-111">Se tiver êxito, os resultados foram gravados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="d3481-111">If it succeeded, results were written to a file.</span></span>

<span data-ttu-id="d3481-112">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="d3481-112">*outputFullFileName* </span></span>  
<span data-ttu-id="d3481-113">Uma cadeia de caracteres COM contianing o nome do arquivo onde os resultados da análise offline foram gravados.</span><span class="sxs-lookup"><span data-stu-id="d3481-113">A COM string contianing the name of the file where offline analysis results were written.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3481-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3481-114">Return value</span></span>

<span data-ttu-id="d3481-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3481-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3481-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3481-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3481-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3481-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d3481-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3481-118">Header</span></span></p></td><td><span data-ttu-id="d3481-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d3481-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d3481-120"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="d3481-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d3481-121">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="d3481-121">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
