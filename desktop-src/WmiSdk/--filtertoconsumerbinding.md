---
description: É usado no registro de consumidores de eventos permanentes para relacionar uma instância do \_ \_ EventConsumer a uma instância de \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: Classe __FilterToConsumerBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798266"
---
# <a name="__filtertoconsumerbinding-class"></a>\_\_Classe FilterToConsumerBinding

A classe de sistema **\_ \_ FilterToConsumerBinding** é usada no registro de consumidores de eventos permanentes para relacionar uma instância do [**\_ \_ EventConsumer**](--eventconsumer.md) a uma instância de [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** é uma classe de associação.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ FilterToConsumerBinding** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ FilterToConsumerBinding** tem essas propriedades.

<dl> <dt>

**Consumidor**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

Referência a uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa o caminho do objeto para um consumidor lógico, o destinatário de um evento. Um consumidor lógico é uma instância de uma classe derivada de **\_ \_ EventConsumer**.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

SID (identificador de segurança) que identifica exclusivamente o usuário que criou a associação. Dependendo do sistema operacional, o WMI armazena o SID do administrador ou o SID do usuário que cria uma instância do **\_ \_ FilterToConsumerBinding**. Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**DeliverSynchronously**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obsoleto. Em vez disso, use a propriedade **DeliveryQoS** no lugar dessa propriedade, porque se **DeliverSynchronously** for definido como **true** , ele substituirá a configuração da propriedade **DeliveryQoS** .

</dd> <dt>

**DeliveryQoS**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Qualidade de serviço para uma assinatura. Se a propriedade **DeliverSynchronously** for definida como **true**, ela substituirá a configuração da propriedade **DeliveryQoS** .

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ SINALIZAr \_ QoS \_ síncrono** (0)


</dt> <dd>

Entrega síncrona

**False**. O evento é entregue ao consumidor lógico de forma síncrona.

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ SINALIZAr \_ QoS \_ Express** (1)


</dt> <dd>

Entrega expressa

**True**. O evento é entregue ao consumidor lógico de forma assíncrona.

</dd> </dl>

</dd> <dt>

**Filter**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ EventFilter**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

Referência a uma instância de [**\_ \_ EventFilter**](--eventfilter.md) que representa o caminho do objeto para um filtro de eventos que é uma consulta que especifica o tipo de evento a ser recebido.

</dd> <dt>

**MaintainSecurityContext**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, os eventos serão entregues no mesmo contexto de segurança em que o provedor estava quando os forneceu.

> [!Note]  
> Somente um consumidor implementado como uma DLL (um consumidor em processo) pode receber eventos no contexto de segurança do provedor. Para obter mais informações sobre provedores em processo e segurança, consulte [hospedagem e segurança do provedor](provider-hosting-and-security.md). Para obter mais informações e exemplos, consulte replace:[recebendo eventos com segurança](receiving-events-securely.md).

 

</dd> <dt>

**SlowDownProviders**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, os provedores serão reduzidos se este consumidor não puder acompanhar.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ FilterToConsumerBinding** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.

Os consumidores de eventos permanentes usam a classe de sistema **\_ \_ FilterToConsumerBinding** para associar filtros de eventos aos consumidores finais. Depois que o filtro e o consumidor são associados, o WMI pode encaminhar eventos que correspondam ao filtro para o consumidor correspondente.

## <a name="examples"></a>Exemplos

O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **\_ \_ FilterToConsumerBinding** como parte de um script complexo para configurar um registro de evento do WMI permanente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_IndicationRelated**](--indicationrelated.md)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Eventos de monitoramento](monitoring-events.md)
</dt> <dt>

[Criando um filtro de eventos](creating-an-event-filter.md)
</dt> <dt>

[Protegendo eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 




