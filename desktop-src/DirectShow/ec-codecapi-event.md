---
description: 'O \_ evento de evento CODECAPI do EC \_ é enviado por um codificador para sinalizar um evento de codificação. O cliente registra o evento de codificador chamando o método ICodecAPI:: RegisterForEvent.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770079"
---
# <a name="ec_codecapi_event"></a><span data-ttu-id="e085e-104">\_evento de CODECAPI do EC \_</span><span class="sxs-lookup"><span data-stu-id="e085e-104">EC\_CODECAPI\_EVENT</span></span>

<span data-ttu-id="e085e-105">O \_ evento de evento CODECAPI do EC \_ é enviado por um codificador para sinalizar um evento de codificação.</span><span class="sxs-lookup"><span data-stu-id="e085e-105">The EC\_CODECAPI\_EVENT event is sent by an encoder to signal an encoding event.</span></span> <span data-ttu-id="e085e-106">O cliente registra o evento de codificador chamando o método [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="e085e-106">The client registers for encoder event by calling the [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="e085e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e085e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e085e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e085e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e085e-109">Dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="e085e-109">User data.</span></span> <span data-ttu-id="e085e-110">O valor desse parâmetro é o ponteiro que o chamador especificou no parâmetro *UserData* do método [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="e085e-110">The value of this parameter is the pointer that the caller specified in the *userData* parameter of the [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

</dd> <dt>

<span data-ttu-id="e085e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e085e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e085e-112">Ponteiro para os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="e085e-112">Pointer to the event data.</span></span> <span data-ttu-id="e085e-113">Esses dados são alocados pelo codificador e devem ser liberados pelo aplicativo, usando a função **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="e085e-113">This data is allocated by the encoder and must be freed by the application, using the **CoTaskMemFree** function.</span></span> <span data-ttu-id="e085e-114">O bloco de dados começa com uma estrutura [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; Converta o parâmetro *lParam2* em um ponteiro para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="e085e-114">The data block starts with a [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) structure; cast the *lParam2* parameter to a pointer to this structure.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e085e-115">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="e085e-115">Default Action</span></span>

<span data-ttu-id="e085e-116">Nenhuma ação padrão.</span><span class="sxs-lookup"><span data-stu-id="e085e-116">No default action.</span></span>

## <a name="requirements"></a><span data-ttu-id="e085e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e085e-117">Requirements</span></span>



| <span data-ttu-id="e085e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e085e-118">Requirement</span></span> | <span data-ttu-id="e085e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e085e-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e085e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e085e-120">Header</span></span><br/> | <dl> <span data-ttu-id="e085e-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e085e-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e085e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e085e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e085e-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="e085e-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e085e-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="e085e-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




