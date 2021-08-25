---
description: A classe SnmpNotification é mapeada da macro do tipo de notificação para uma classe CIM encapsulada.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: Classe SnmpNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: be0847c7a7d96fb7491274350c828d0cc319240823fa006e972bb295ad477773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860356"
---
# <a name="snmpnotification-class"></a>Classe SnmpNotification

A classe **SnmpNotification** é mapeada da macro do [tipo de notificação](notification-type-macro.md) para uma classe CIM encapsulada. É uma classe base usada pelo [provedor SNMP](snmp-provider.md) para qualquer classe mapeada da macro do [tipo de notificação](notification-type-macro.md) para uma classe CIM encapsulada pelo provedor SNMP.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

## <a name="syntax"></a>Sintaxe

``` syntax
class SnmpNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a>Membros

A classe **SnmpNotification** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SnmpNotification** tem essas propriedades.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço de rede da entidade que criou a notificação. Esse é o endereço real do dispositivo. Quando a entidade de gerenciamento usa SNMP sobre UDP, o endereço de transporte se refere a um endereço IP. Quando a entidade de gerenciamento usa SNMP sobre IPX, o endereço de transporte é definido como **nulo**. Esta propriedade é válida somente para SNMPv1.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Protocolo de transporte usado pela entidade de envio. Essa propriedade é válida para SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço de rede da entidade que enviou a notificação. Este é o endereço da última entidade que encaminhou a notificação. Quando a entidade de gerenciamento usa SNMP sobre UDP, o endereço de transporte se refere a um endereço IP. Quando a entidade de gerenciamento usa SNMP sobre IPX, o endereço de transporte se refere a um Endereço IPX. Essa propriedade é válida para SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O protocolo de transporte usado pela entidade de envio.

</dd> <dt>

**Comunidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Community nome associado a uma instância do PDU. O nome da Comunidade autentica o originador da PDU. Essa propriedade é válida para SNMPv1 e SNMPv2C.

</dd> <dt>

**Identificação**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **\_ Convenção de texto** ("objectidentifier"), **codificação** ("objectidentifier") **, \_ sintaxe de objeto** ("objectidentifier"), **\_ identificador de objeto** ("1.3.6.1.6.3.1.1.4.1")
</dt> </dl>

Identificação autoritativa desta notificação. Mapas diretamente à associação de variável SnmpTrapOID. Esta propriedade é válida somente para o SNMPv2C.

</dd> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md). Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](wmi-security-constants.md).

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Estampa**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **\_ Convenção de texto** ("timetiques"), **codificação** ("timetiques") **, \_ sintaxe de objeto** ("timetiques"), **\_ identificador de objeto** ("1.3.6.1.2.1.1.3")
</dt> </dl>

Tempo em centésimos de um segundo desde que a parte de gerenciamento de rede do agente foi reinicializada pela última vez. A variável MIB sysUptime. 0, que é do tipo **INTEGER32**. Essa propriedade é mapeada para o carimbo de **data/hora** da propriedade de classe CIM, que é do tipo **UInt32**. Esta propriedade é válida somente para o SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro de [tipo de objeto](object-type-macro.md) chamada **timestamp** ou **Identification** causa um conflito de mapeamento. Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.

uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro [de tipo de objeto](object-type-macro.md) chamada **Community** causa um conflito de mapeamento. Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>   |
| Namespace<br/>                | \\Localhost SNMP \\ raiz<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[Macro do tipo de notificação](notification-type-macro.md)
</dt> </dl>

 

