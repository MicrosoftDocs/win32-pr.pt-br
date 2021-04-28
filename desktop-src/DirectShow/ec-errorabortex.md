---
description: EC_ERRORABORTEX-uma operação foi anulada devido a um erro.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3bf1e1f24f9d5b07312f542c1ce4ea671f601d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094604"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="861d5-103">ERRORABORTEX do EC \_</span><span class="sxs-lookup"><span data-stu-id="861d5-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="861d5-104">Uma operação foi anulada devido a um erro.</span><span class="sxs-lookup"><span data-stu-id="861d5-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="861d5-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="861d5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="861d5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="861d5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="861d5-107">**(HRESULT)** Código de falha da operação que falhou.</span><span class="sxs-lookup"><span data-stu-id="861d5-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="861d5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="861d5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="861d5-109">**(BSTR)** Cadeia de caracteres que contém informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="861d5-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="861d5-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="861d5-110">Default Action</span></span>

<span data-ttu-id="861d5-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="861d5-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="861d5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="861d5-112">Remarks</span></span>

<span data-ttu-id="861d5-113">O filtro de [origem do Windows Media](windows-media-source-filter.md) herdado envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="861d5-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="861d5-114">Os novos filtros não devem enviar esse evento.</span><span class="sxs-lookup"><span data-stu-id="861d5-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="861d5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="861d5-115">Requirements</span></span>



| <span data-ttu-id="861d5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="861d5-116">Requirement</span></span> | <span data-ttu-id="861d5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="861d5-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="861d5-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="861d5-118">Header</span></span><br/> | <dl> <span data-ttu-id="861d5-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="861d5-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="861d5-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="861d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="861d5-121">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="861d5-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="861d5-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="861d5-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




