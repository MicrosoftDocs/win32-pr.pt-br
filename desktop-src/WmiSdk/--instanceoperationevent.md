---
description: Serve como uma classe base para todos os eventos intrínsecos relacionados a uma instância.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: Classe __InstanceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807876"
---
# <a name="__instanceoperationevent-class"></a>\_\_Classe InstanceOperationEvent

A classe de sistema **\_ \_ InstanceOperationEvent** serve como uma classe base para todos os eventos intrínsecos relacionados a uma instância.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ InstanceOperationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ InstanceOperationEvent** tem essas propriedades.

<dl> <dt>

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

Instância afetada pelo evento. Para eventos de criação, essa é a instância recém-criada. Para eventos de modificação, esta é a nova versão da instância alterada. Para eventos de exclusão, essa é a instância excluída.

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

A classe **\_ \_ InstanceOperationEvent** é derivada de [**\_ \_ Event**](--event.md).

As instâncias de **\_ \_ InstanceOperationEvent** não são criadas; apenas instâncias de suas subclasses são criadas. As classes a seguir derivam de **\_ \_ InstanceOperationEvent**:

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**Visão geral**

Assim como há uma classe WMI que representa cada tipo de recurso do sistema que pode ser gerenciado usando o WMI, há uma classe WMI que representa cada tipo de evento WMI. Quando ocorre um evento que pode ser monitorado pelo WMI, uma instância da classe de evento WMI correspondente é criada. Um evento WMI ocorre quando essa instância é criada.

Há três tipos principais de classes de evento WMI, todas derivadas da classe WMI de [**\_ \_ evento**](--event.md) : eventos intrínsecos, eventos extrínsecos e eventos de temporizador. Os eventos intrínsecos, por sua vez, são representados por três classes distintas derivadas da classe de **\_ \_ evento** : [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** e [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

Eventos intrínsecos

Os eventos intrínsecos são usados para monitorar um recurso representado por uma classe no repositório CIM. Cada recurso é representado por uma instância de uma classe. Isso significa que o monitoramento de um recurso usando o WMI, na verdade, envolve o monitoramento das instâncias que correspondem ao recurso.

Eventos intrínsecos também podem ser usados para monitorar alterações em um namespace ou classe no repositório. No entanto, o monitoramento de alterações em namespaces ou classes é de valor limitado para administradores do sistema.

Um evento intrínseco é representado por uma instância de uma classe derivada de \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent ou \_ \_ ClassOperationEvent. As alterações nas instâncias no WMI são representadas pela \_ \_ classe InstanceOperationEvent e pelas classes derivadas dela: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent e \_ \_ InstanceDeletionEvent.

Os recursos de monitoramento usando o WMI envolvem instâncias de monitoramento e todas as alterações feitas em instâncias são representadas por \_ \_ InstanceOperationEvent e pelas classes derivadas dela. Isso significa que os recursos de monitoramento em última instância envolvem o monitoramento de instâncias de \_ \_ classes derivadas de InstanceOperationEvent.

Você registra o interesse em instâncias de uma dessas classes emitindo uma consulta de notificação expressa na WQL. A consulta usa sintaxe semelhante à seguinte:

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Para obter uma discussão mais demorada sobre como usar os eventos da instância WMI para monitorar a atividade do computador, consulte [como posso monitorar diferentes tipos de eventos com apenas um script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Exemplos

O exemplo de código do [evento monitor Process](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript na galeria do TechNet usa **\_ \_ InstanceOperationEvent** para monitorar o primeiro evento de instância WMI para o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Gravando em um arquivo de log baseado em um evento](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

