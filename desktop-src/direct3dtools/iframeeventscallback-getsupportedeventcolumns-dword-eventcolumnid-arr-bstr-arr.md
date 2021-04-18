---
description: Obtém informações sobre quais colunas (tipos de dados de evento) têm suporte na lista de eventos.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameEventsCallback:: GetSupportedEventColumns'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5b7bc9f74998a061ea63fca925263b7b4a0a4d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456680"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span data-ttu-id="f99cd-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>Método IFrameEventsCallback:: GetSupportedEventColumns</span><span class="sxs-lookup"><span data-stu-id="f99cd-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback::GetSupportedEventColumns method</span></span>

<span data-ttu-id="f99cd-104">Obtém informações sobre quais colunas (tipos de dados de evento) têm suporte na lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f99cd-104">Gets information about which columns (types of event data) are supported by the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f99cd-105">Syntax</span></span>


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="f99cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f99cd-106">Parameters</span></span>

<span data-ttu-id="f99cd-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="f99cd-107">*numColumns* </span></span>  
<span data-ttu-id="f99cd-108">O número de colunas com suporte no</span><span class="sxs-lookup"><span data-stu-id="f99cd-108">The number of columns supported by</span></span>

<span data-ttu-id="f99cd-109">*\_pIDs count0* </span><span class="sxs-lookup"><span data-stu-id="f99cd-109">*count0\_pIDs* </span></span>  
<span data-ttu-id="f99cd-110">As IDs de cada coluna com suporte na lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f99cd-110">The IDs of each column supported by the event list.</span></span>

<span data-ttu-id="f99cd-111">*count0 \_ pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="f99cd-111">*count0\_pBstrNames* </span></span>  
<span data-ttu-id="f99cd-112">Os nomes de cada coluna, como uma cadeia de caracteres COM, com suporte na lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f99cd-112">The names of each column, as a COM string, supported by the event list.</span></span>

## <a name="return-value"></a><span data-ttu-id="f99cd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f99cd-113">Return value</span></span>

<span data-ttu-id="f99cd-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f99cd-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f99cd-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f99cd-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f99cd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f99cd-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f99cd-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f99cd-117">Header</span></span></p></td><td><span data-ttu-id="f99cd-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f99cd-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f99cd-119"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="f99cd-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f99cd-120">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="f99cd-120">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
