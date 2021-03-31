---
description: Evento de rastreamento de rede Winsock para operação de fechamento de soquete.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647146"
---
# <a name="afd_event_close-event"></a><span data-ttu-id="93971-103">Evento de fechamento de \_ evento de AFD \_</span><span class="sxs-lookup"><span data-stu-id="93971-103">AFD\_EVENT\_CLOSE event</span></span>

<span data-ttu-id="93971-104">O evento de **\_ \_ fechamento de evento de AFD** é um evento de rastreamento de rede do Winsock para a operação de fechamento de soquete.</span><span class="sxs-lookup"><span data-stu-id="93971-104">The **AFD\_EVENT\_CLOSE** event is a Winsock network tracing event for socket close operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="93971-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93971-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93971-106">*EnterExit*</span><span class="sxs-lookup"><span data-stu-id="93971-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="93971-107">Informações sobre este evento.</span><span class="sxs-lookup"><span data-stu-id="93971-107">Information on this event.</span></span>

<span data-ttu-id="93971-108">A tabela a seguir lista os possíveis valores para o parâmetro *EnterExit* :</span><span class="sxs-lookup"><span data-stu-id="93971-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="93971-109">Valor</span><span class="sxs-lookup"><span data-stu-id="93971-109">Value</span></span>                                                                        | <span data-ttu-id="93971-110">Significado</span><span class="sxs-lookup"><span data-stu-id="93971-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93971-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="93971-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="93971-112">O início de uma solicitação do Winsock.</span><span class="sxs-lookup"><span data-stu-id="93971-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="93971-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="93971-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="93971-114">A solicitação do Winsock foi concluída.</span><span class="sxs-lookup"><span data-stu-id="93971-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="93971-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93971-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="93971-116">O driver do Winsock AFD realizou uma ação interna (anulando uma conexão, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="93971-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="93971-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="93971-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="93971-118">O driver TCP/IP fez com que esse evento ocorresse.</span><span class="sxs-lookup"><span data-stu-id="93971-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="93971-119">Isso geralmente indica uma notificação de dados.</span><span class="sxs-lookup"><span data-stu-id="93971-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="93971-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="93971-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="93971-121">O driver do Winsock AFD fez com que esse evento ocorresse (definindo uma opção de soquete, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="93971-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="93971-122">*Localidade*</span><span class="sxs-lookup"><span data-stu-id="93971-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="93971-123">Um campo privado usado internamente.</span><span class="sxs-lookup"><span data-stu-id="93971-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="93971-124">*Processo*</span><span class="sxs-lookup"><span data-stu-id="93971-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="93971-125">O endereço [EPROCESS](/windows-hardware/drivers/kernel/eprocess) do processo que possui o soquete relacionado.</span><span class="sxs-lookup"><span data-stu-id="93971-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="93971-126">Essa é uma estrutura opaca que serve como o objeto de processo para um processo.</span><span class="sxs-lookup"><span data-stu-id="93971-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="93971-127">Para obter mais informações, consulte a documentação do Windows Driver Kit para a estrutura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .</span><span class="sxs-lookup"><span data-stu-id="93971-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93971-128">*Ponto de extremidade*</span><span class="sxs-lookup"><span data-stu-id="93971-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="93971-129">O \_ endereço do ponto de extremidade de AFD do soquete.</span><span class="sxs-lookup"><span data-stu-id="93971-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="93971-130">*Status*</span><span class="sxs-lookup"><span data-stu-id="93971-130">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="93971-131">O código NTSTATUS para a operação.</span><span class="sxs-lookup"><span data-stu-id="93971-131">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93971-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="93971-132">Remarks</span></span>

<span data-ttu-id="93971-133">O evento de **\_ \_ fechamento de evento de AFD** é rastreado para uma operação de rede Winsock para fechar um soquete.</span><span class="sxs-lookup"><span data-stu-id="93971-133">The **AFD\_EVENT\_CLOSE** event is traced for a Winsock network operation to close a socket.</span></span> <span data-ttu-id="93971-134">O canal para esse evento é o Winsock-AFD.</span><span class="sxs-lookup"><span data-stu-id="93971-134">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="93971-135">O nível desse evento é informativo.</span><span class="sxs-lookup"><span data-stu-id="93971-135">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="93971-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93971-136">Requirements</span></span>



| <span data-ttu-id="93971-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="93971-137">Requirement</span></span> | <span data-ttu-id="93971-138">Valor</span><span class="sxs-lookup"><span data-stu-id="93971-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="93971-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93971-139">Minimum supported client</span></span><br/> | <span data-ttu-id="93971-140">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="93971-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="93971-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93971-141">Minimum supported server</span></span><br/> | <span data-ttu-id="93971-142">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="93971-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93971-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="93971-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93971-144">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="93971-144">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="93971-145">**\_descritor de evento**</span><span class="sxs-lookup"><span data-stu-id="93971-145">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="93971-146">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="93971-146">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="93971-147">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="93971-147">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="93971-148">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="93971-148">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

