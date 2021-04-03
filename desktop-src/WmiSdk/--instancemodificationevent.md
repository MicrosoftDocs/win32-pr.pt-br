---
description: Relata um evento de modificação de instância, que é um tipo de evento intrínseco gerado quando uma instância é alterada no namespace.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: Classe __InstanceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829282"
---
# <a name="__instancemodificationevent-class"></a>\_\_Classe InstanceModificationEvent

A classe de sistema **\_ \_ InstanceModificationEvent** relata um evento de modificação de instância, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando uma instância é alterada no namespace.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ InstanceModificationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ InstanceModificationEvent** tem essas propriedades.

<dl> <dt>

**PreviousInstance**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cópia da instância antes da modificação.

</dd> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nova versão da instância alterada. Essa propriedade é herdada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ InstanceModificationEvent** é derivada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Modificação de um recurso: \_ \_ InstanceModificationEvent**

Suponha que você suspeite que um aplicativo de gerenciamento que você está usando está alterando erroneamente o tipo de inicialização de um serviço em um de seus servidores. Você deseja escrever um script WMI para monitorar as modificações feitas na configuração do serviço. Assim que uma modificação é feita em um serviço, seu TargetInstance correspondente reflete a modificação.

Se você registrar seu interesse nesse evento, uma modificação na configuração do serviço resultará na criação de uma instância da classe **\_ \_ InstanceModificationEvent** .

As consultas de notificação que solicitam a notificação da modificação de um recurso e usam eventos intrínsecos usam uma sintaxe semelhante à seguinte:

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>Exemplos

O exemplo de teste de [evento do monitor de modificação do processo](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) na galeria do TechNet usa **\_ \_ InstanceModificationEvent** para monitorar a primeira ocorrência de um evento de modificação da instância do WMI para o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

