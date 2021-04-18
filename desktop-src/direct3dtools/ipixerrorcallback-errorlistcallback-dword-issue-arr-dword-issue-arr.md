---
description: Um retorno de chamada que notifica o host de erros retornados pela solicitação associada.
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixErrorCallback:: ErrorListCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808365"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span data-ttu-id="a73a2-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>Método IPixErrorCallback:: ErrorListCallback</span><span class="sxs-lookup"><span data-stu-id="a73a2-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback::ErrorListCallback method</span></span>

<span data-ttu-id="a73a2-104">Um retorno de chamada que notifica o host de erros retornados pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="a73a2-104">A callback that notifies the host of errors returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a73a2-105">Syntax</span></span>


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a><span data-ttu-id="a73a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a73a2-106">Parameters</span></span>

<span data-ttu-id="a73a2-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="a73a2-107">*count* </span></span>  
<span data-ttu-id="a73a2-108">O número de erros.</span><span class="sxs-lookup"><span data-stu-id="a73a2-108">The number of errors.</span></span>

<span data-ttu-id="a73a2-109">*count0 \_ errorList* </span><span class="sxs-lookup"><span data-stu-id="a73a2-109">*count0\_errorList* </span></span>  
<span data-ttu-id="a73a2-110">Os erros.</span><span class="sxs-lookup"><span data-stu-id="a73a2-110">The errors.</span></span>

<span data-ttu-id="a73a2-111">*contar* </span><span class="sxs-lookup"><span data-stu-id="a73a2-111">*count* </span></span>  
<span data-ttu-id="a73a2-112">O número de avisos.</span><span class="sxs-lookup"><span data-stu-id="a73a2-112">The number of warningns.</span></span>

<span data-ttu-id="a73a2-113">*count0 de \_ avisos* </span><span class="sxs-lookup"><span data-stu-id="a73a2-113">*count0\_warningList* </span></span>  
<span data-ttu-id="a73a2-114">Os avisos.</span><span class="sxs-lookup"><span data-stu-id="a73a2-114">The warnings.</span></span>

## <a name="return-value"></a><span data-ttu-id="a73a2-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a73a2-115">Return value</span></span>

<span data-ttu-id="a73a2-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a73a2-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a73a2-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a73a2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73a2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a73a2-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a73a2-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a73a2-119">Header</span></span></p></td><td><span data-ttu-id="a73a2-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a73a2-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a73a2-121"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="a73a2-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a73a2-122">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="a73a2-122">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
