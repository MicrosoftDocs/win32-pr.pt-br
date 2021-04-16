---
description: Um retorno de chamada que notifica o host de mensagens retornadas pela solicitação associada.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixErrorCallback:: MessagesCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105772676"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span data-ttu-id="a6852-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>Método IPixErrorCallback:: MessagesCallback</span><span class="sxs-lookup"><span data-stu-id="a6852-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback::MessagesCallback method</span></span>

<span data-ttu-id="a6852-104">Um retorno de chamada que notifica o host de mensagens retornadas pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="a6852-104">A callback that notifies the host of messages returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6852-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6852-105">Syntax</span></span>


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a><span data-ttu-id="a6852-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6852-106">Parameters</span></span>

<span data-ttu-id="a6852-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="a6852-107">*count* </span></span>  
<span data-ttu-id="a6852-108">O número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a6852-108">The number of messages.</span></span>

<span data-ttu-id="a6852-109">*\_mensagens count0* </span><span class="sxs-lookup"><span data-stu-id="a6852-109">*count0\_messages* </span></span>  
<span data-ttu-id="a6852-110">As mensagens.</span><span class="sxs-lookup"><span data-stu-id="a6852-110">The messages.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6852-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6852-111">Return value</span></span>

<span data-ttu-id="a6852-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a6852-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a6852-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6852-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6852-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6852-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a6852-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6852-115">Header</span></span></p></td><td><span data-ttu-id="a6852-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a6852-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a6852-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="a6852-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a6852-118">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="a6852-118">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
