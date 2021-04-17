---
description: Enviado pelo filtro do gravador ASF do WM quando ele conclui o pré-processamento para codificação de passagem.
ms.assetid: 2029afc4-419c-494a-ae52-1f84b08bcb35
title: EC_PREPROCESS_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba13938ac848ef37f1a2a2826372d97ff5a5d716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768648"
---
# <a name="ec_preprocess_complete"></a><span data-ttu-id="c0a69-103">pré-processamento de EC \_ \_ concluído</span><span class="sxs-lookup"><span data-stu-id="c0a69-103">EC\_PREPROCESS\_COMPLETE</span></span>

<span data-ttu-id="c0a69-104">Enviado pelo filtro do [gravador ASF do WM](wm-asf-writer-filter.md) quando ele conclui o pré-processamento para codificação de passagem.</span><span class="sxs-lookup"><span data-stu-id="c0a69-104">Sent by the [WM ASF Writer](wm-asf-writer-filter.md) filter when it completes the pre-processing for multipass encoding.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0a69-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0a69-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0a69-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c0a69-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c0a69-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="c0a69-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0a69-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c0a69-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c0a69-109">(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro.</span><span class="sxs-lookup"><span data-stu-id="c0a69-109">(**IUnknown**\*) Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c0a69-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="c0a69-110">Default Action</span></span>

<span data-ttu-id="c0a69-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c0a69-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a69-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0a69-112">Requirements</span></span>



| <span data-ttu-id="c0a69-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a69-113">Requirement</span></span> | <span data-ttu-id="c0a69-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c0a69-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a69-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0a69-115">Header</span></span><br/> | <dl> <span data-ttu-id="c0a69-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0a69-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0a69-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0a69-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a69-118">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="c0a69-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c0a69-119">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="c0a69-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




