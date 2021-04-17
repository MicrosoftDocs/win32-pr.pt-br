---
description: A classe SnmpExtendedNotification é a classe base para qualquer classe mapeada da macro do tipo de notificação para uma classe CIM pelo provedor SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: Classe SnmpExtendedNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798482"
---
# <a name="snmpextendednotification-class"></a>Classe SnmpExtendedNotification

A classe **SnmpExtendedNotification** é a classe base para qualquer classe mapeada da macro do [tipo de notificação](notification-type-macro.md) para uma classe CIM pelo [provedor SNMP](snmp-provider.md).

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
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

A classe **SnmpExtendedNotification** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SnmpExtendedNotification** tem essas propriedades.

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

Nome da Comunidade associado a uma instância do PDU. O nome da Comunidade autentica o originador da PDU. Essa propriedade é válida para SNMPv1 e SNMPv2C.

</dd> <dt>

**Identificação**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **\_ Convenção de texto** ("objectidentifier"), **codificação** ("objectidentifier") **, \_ sintaxe de objeto** ("objectidentifier"), **\_ identificador de objeto** ("1.3.6.1.6.3.1.1.4.1")
</dt> </dl>

Identificação autoritativa desta notificação. Mapeia diretamente para a associação de variável SnmpTrapOID de entrada MIB. Esta propriedade é válida somente para o SNMPv2C.

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

Tempo em centésimos de um segundo desde que a parte de gerenciamento de rede do agente foi reinicializada pela última vez. Isso é mapeado para a variável MIB sysUptime. 0, que é do tipo **INTEGER32**. Essa propriedade é mapeada para o carimbo de **data/hora** da propriedade de classe CIM, que é do tipo **UInt32**. Esta propriedade é válida somente para o SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro de [tipo de objeto](object-type-macro.md) chamada **timestamp** ou **Identification** causa um conflito de mapeamento. Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.

Uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro de [tipo de objeto](object-type-macro.md) chamada **Community** causa um conflito de mapeamento. Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ SNMP \\ Smir<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[Macro do tipo de notificação](notification-type-macro.md)
</dt> </dl>

 

