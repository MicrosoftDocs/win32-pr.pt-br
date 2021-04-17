---
description: Uma função de retorno de chamada usada para notificar o host das informações de resumo do log de gráficos.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ISummaryCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812048"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span data-ttu-id="2cb8b-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>Método ISummaryCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="2cb8b-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback::ResultCallback method</span></span>

<span data-ttu-id="2cb8b-104">Uma função de retorno de chamada usada para notificar o host das informações de resumo do log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-104">A callback function used to notify the host of graphics log summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb8b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cb8b-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a><span data-ttu-id="2cb8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cb8b-106">Parameters</span></span>

<span data-ttu-id="2cb8b-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="2cb8b-107">*count* </span></span>  
<span data-ttu-id="2cb8b-108">O número de itens de informações de resumo retornados.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-108">The number of summary information items returned.</span></span>

<span data-ttu-id="2cb8b-109">*count0 \_ summaryItem* </span><span class="sxs-lookup"><span data-stu-id="2cb8b-109">*count0\_summaryItem* </span></span>  
<span data-ttu-id="2cb8b-110">Os itens de informações de resumo (pares chave-valor).</span><span class="sxs-lookup"><span data-stu-id="2cb8b-110">The summary information items (key-value pairs).</span></span>

## <a name="return-value"></a><span data-ttu-id="2cb8b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cb8b-111">Return value</span></span>

<span data-ttu-id="2cb8b-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2cb8b-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2cb8b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb8b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cb8b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2cb8b-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2cb8b-115">Header</span></span></p></td><td><span data-ttu-id="2cb8b-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2cb8b-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2cb8b-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="2cb8b-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2cb8b-118">**ISummaryCallback**</span><span class="sxs-lookup"><span data-stu-id="2cb8b-118">**ISummaryCallback**</span></span>](/windows/desktop/direct3dtools/isummarycallback)

 

 
