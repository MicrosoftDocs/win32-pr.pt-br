---
description: O seguinte mostra as constantes de segurança do WMI usadas para eventos. Eles são usados para definir ACEs (entradas de controle de acesso) em descritores de segurança usados para eventos ou coletores.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Constantes de segurança de evento (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091374"
---
# <a name="event-security-constants"></a><span data-ttu-id="c7c72-104">Constantes de segurança de evento</span><span class="sxs-lookup"><span data-stu-id="c7c72-104">Event Security Constants</span></span>

<span data-ttu-id="c7c72-105">O seguinte mostra as constantes de segurança do WMI usadas para eventos.</span><span class="sxs-lookup"><span data-stu-id="c7c72-105">The following shows the WMI security constants used for events.</span></span> <span data-ttu-id="c7c72-106">Eles são usados para definir ACEs (entradas de controle de acesso) em descritores de segurança usados para eventos ou coletores.</span><span class="sxs-lookup"><span data-stu-id="c7c72-106">They are used to set access control entries (ACEs) in security descriptors used for events or sinks.</span></span>

<dl> <dt>

<span data-ttu-id="c7c72-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_publicação do WBEM à direita \_**</span><span class="sxs-lookup"><span data-stu-id="c7c72-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM\_RIGHT\_PUBLISH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c72-108">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="c7c72-108">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="c7c72-109">Especifica que a conta pode publicar eventos na instância de [**\_ \_ EventFilter**](--eventfilter.md) que define o filtro de eventos para um consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="c7c72-109">Specifies that the account can publish events to the instance of [**\_\_EventFilter**](--eventfilter.md) that defines the event filter for a permanent consumer.</span></span> <span data-ttu-id="c7c72-110">Disponível em wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="c7c72-110">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7c72-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**\_assinatura do WBEM direito \_**</span><span class="sxs-lookup"><span data-stu-id="c7c72-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM\_RIGHT\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c72-112">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="c7c72-112">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="c7c72-113">Especifica que um consumidor pode assinar os eventos entregues a um coletor.</span><span class="sxs-lookup"><span data-stu-id="c7c72-113">Specifies that a consumer can subscribe to the events delivered to a sink.</span></span> <span data-ttu-id="c7c72-114">Usado em [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span><span class="sxs-lookup"><span data-stu-id="c7c72-114">Used in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span></span> <span data-ttu-id="c7c72-115">Disponível em wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="c7c72-115">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7c72-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ sujeitos \_ a \_ SDS**</span><span class="sxs-lookup"><span data-stu-id="c7c72-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM\_S\_SUBJECT\_TO\_SDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c72-117">274435 (0x43003)</span><span class="sxs-lookup"><span data-stu-id="c7c72-117">274435 (0x43003)</span></span>
</dt> <dt>



<span data-ttu-id="c7c72-118">O provedor de eventos indica que o WMI verifica a propriedade do **\_ descritor de segurança** em cada evento (herdado do [**\_ \_ evento**](--event.md)) e apenas envia eventos aos consumidores com as permissões de acesso apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c7c72-118">Event provider indicates that WMI checks the **SECURITY\_DESCRIPTOR** property in each event (inherited from [**\_\_Event**](--event.md)), and only sends events to consumers with the appropriate access permissions.</span></span> <span data-ttu-id="c7c72-119">Disponível em wbemprov. h.</span><span class="sxs-lookup"><span data-stu-id="c7c72-119">Available in wbemprov.h.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7c72-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c72-120">Requirements</span></span>



| <span data-ttu-id="c7c72-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c72-121">Requirement</span></span> | <span data-ttu-id="c7c72-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7c72-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c72-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c72-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c72-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7c72-124">Windows Vista</span></span><br/>                                                                                                                               |
| <span data-ttu-id="c7c72-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c72-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c72-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7c72-126">Windows Server 2008</span></span><br/>                                                                                                                         |
| <span data-ttu-id="c7c72-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7c72-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c72-128"><dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c72-128"><dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c72-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7c72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c72-130">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="c7c72-130">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="c7c72-131">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="c7c72-131">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="c7c72-132">Protegendo eventos WMI</span><span class="sxs-lookup"><span data-stu-id="c7c72-132">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




