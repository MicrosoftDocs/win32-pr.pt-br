---
description: O seguinte mostra as constantes de segurança do WMI usadas para eventos. Eles são usados para definir ACEs (entradas de controle de acesso) em descritores de segurança usados para eventos ou coletores.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Constantes de segurança de evento (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ae26364c7edf6daaf9b70dcf769675c0a39966286b3b8f725fefe0af73ff8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244286"
---
# <a name="event-security-constants"></a>Constantes de segurança de evento

O seguinte mostra as constantes de segurança do WMI usadas para eventos. Eles são usados para definir ACEs (entradas de controle de acesso) em descritores de segurança usados para eventos ou coletores.

<dl> <dt>

<span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_publicação do WBEM à direita \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Especifica que a conta pode publicar eventos na instância de [**\_ \_ EventFilter**](--eventfilter.md) que define o filtro de eventos para um consumidor permanente. Disponível em wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**\_assinatura do WBEM direito \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Especifica que um consumidor pode assinar os eventos entregues a um coletor. Usado em [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity). Disponível em wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ sujeitos \_ a \_ SDS**
</dt> <dd> <dl> <dt>

274435 (0x43003)
</dt> <dt>



O provedor de eventos indica que o WMI verifica a propriedade do **\_ descritor de segurança** em cada evento (herdado do [**\_ \_ evento**](--event.md)) e apenas envia eventos aos consumidores com as permissões de acesso apropriadas. Disponível em wbemprov. h.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> <dt>

[Protegendo eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 




