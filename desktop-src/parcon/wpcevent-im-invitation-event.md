---
description: Evento por usuário fornecido para o log de inicialização de conversas por clientes de mensagens instantâneas.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: WPCEVENT_IM_INVITATION evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768307"
---
# <a name="wpcevent_im_invitation-event"></a><span data-ttu-id="adf8a-103">Evento de convite do WPCEVENT \_ im \_</span><span class="sxs-lookup"><span data-stu-id="adf8a-103">WPCEVENT\_IM\_INVITATION event</span></span>

<span data-ttu-id="adf8a-104">Evento por usuário fornecido para o log de inicialização de conversas por clientes de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="adf8a-104">Per-user event provided for logging initiation of conversations by Instant Messaging clients.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="adf8a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adf8a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf8a-106">*AppName*</span><span class="sxs-lookup"><span data-stu-id="adf8a-106">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-107">O nome do aplicativo que está gerando o evento.</span><span class="sxs-lookup"><span data-stu-id="adf8a-107">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-108">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="adf8a-108">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-109">A cadeia de caracteres da versão do aplicativo que está gerando o evento.</span><span class="sxs-lookup"><span data-stu-id="adf8a-109">The version string for the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-110">*AccountName*</span><span class="sxs-lookup"><span data-stu-id="adf8a-110">*AccountName*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-111">A cadeia de caracteres de identidade da conta de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="adf8a-111">The instant messaging account identity string.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-112">*Convid*</span><span class="sxs-lookup"><span data-stu-id="adf8a-112">*ConvID*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-113">O identificador da conversa.</span><span class="sxs-lookup"><span data-stu-id="adf8a-113">The identifier for the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-114">*RequestingIP*</span><span class="sxs-lookup"><span data-stu-id="adf8a-114">*RequestingIP*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-115">Uma cadeia de caracteres que contém o endereço IP do computador que está enviando o convite.</span><span class="sxs-lookup"><span data-stu-id="adf8a-115">A string that contains the IP address of the computer that is sending the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-116">*Remetente*</span><span class="sxs-lookup"><span data-stu-id="adf8a-116">*Sender*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-117">A cadeia de caracteres de identidade da conta de mensagens instantâneas para a conta que está emitindo o convite.</span><span class="sxs-lookup"><span data-stu-id="adf8a-117">The instant messaging account identity string for the account that is issuing the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-118">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="adf8a-118">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-119">Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="adf8a-119">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-120">*RecipCount*</span><span class="sxs-lookup"><span data-stu-id="adf8a-120">*RecipCount*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-121">A contagem de destinatários que estão recebendo o convite e que têm identidades definidas no campo destinatário.</span><span class="sxs-lookup"><span data-stu-id="adf8a-121">The count of recipients who are receiving the invitation and who have identities defined in the recipient field.</span></span>

</dd> <dt>

<span data-ttu-id="adf8a-122">*Destinatário*</span><span class="sxs-lookup"><span data-stu-id="adf8a-122">*Recipient*</span></span> 
</dt> <dd>

<span data-ttu-id="adf8a-123">Uma cadeia delimitada que contém cadeias de caracteres de identidade da conta de mensagens instantâneas para os destinatários do convite.</span><span class="sxs-lookup"><span data-stu-id="adf8a-123">A delimited string that contains instant messaging account identity strings for the recipients of the invitation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adf8a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adf8a-124">Requirements</span></span>



| <span data-ttu-id="adf8a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf8a-125">Requirement</span></span> | <span data-ttu-id="adf8a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="adf8a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adf8a-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf8a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="adf8a-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="adf8a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="adf8a-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf8a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="adf8a-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="adf8a-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="adf8a-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="adf8a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf8a-132"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf8a-132"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf8a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="adf8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf8a-134">Usando APIs de log para controles dos pais</span><span class="sxs-lookup"><span data-stu-id="adf8a-134">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="adf8a-135">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="adf8a-135">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




