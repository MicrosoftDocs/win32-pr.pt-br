---
description: Serve como uma classe base para todos os eventos intrínsecos relacionados a uma instância.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent classe
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
ms.openlocfilehash: a4e988f26b64d0d8bd4a23f853b7bf9dc92f2610936239b4363439d5c7d70170
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320803"
---
# <a name="__instanceoperationevent-class"></a>\_\_Classe InstanceOperationEvent

A **\_ \_ classe de sistema InstanceOperationEvent** serve como uma classe base para todos os eventos intrínsecos relacionados a uma instância.

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

A **\_ \_ classe InstanceOperationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe InstanceOperationEvent** tem essas propriedades.

<dl> <dt>

**DESCRITOR \_ DE SEGURANÇA**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Essa propriedade é herdada do [**\_ \_ Evento**](--event.md).

</dd> <dt>

**Targetinstance**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Instância afetada pelo evento. Para eventos de criação, essa é a instância recém-criada. Para eventos de modificação, essa é a nova versão da instância alterada. Para eventos de exclusão, essa é a instância excluída.

</dd> <dt>

**TEMPO \_ CRIADO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Esse é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (Tempos Universais Coordenados). Essa propriedade é herdada do [**\_ \_ Evento**](--event.md).

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\_ \_ classe InstanceOperationEvent** é derivada de [**\_ \_ Event**](--event.md).

Instâncias de **\_ \_ InstanceOperationEvent** não são criadas; somente instâncias de suas subclasses são criadas. As classes a seguir derivam **\_ \_ de InstanceOperationEvent**:

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**Visão geral**

Assim como há uma classe WMI que representa cada tipo de recurso do sistema que pode ser gerenciado usando WMI, há uma classe WMI que representa cada tipo de evento WMI. Quando ocorre um evento que pode ser monitorado pelo WMI, uma instância da classe de evento WMI correspondente é criada. Um evento WMI ocorre quando essa instância é criada.

Há três tipos principais de classes de evento WMI, todos derivados da classe [**\_ \_ WMI**](--event.md) de evento: Eventos Intrínsecos, Eventos Extrínsecos e Eventos de Temporizador. Os Eventos Intrínsecos, por sua vez, **\_ \_** são representados por três classes distintas derivadas da classe Event: [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** e [**\_ \_ ClassOperationEvent.**](--classoperationevent.md)

Eventos intrínsecos

Eventos intrínsecos são usados para monitorar um recurso representado por uma classe no repositório CIM. Cada recurso é representado por uma instância de uma classe. Isso significa que o monitoramento de um recurso usando o WMI, na verdade, envolve o monitoramento das instâncias que correspondem ao recurso.

Eventos intrínsecos também podem ser usados para monitorar alterações em um namespace ou classe no repositório. No entanto, o monitoramento de alterações em namespaces ou classes é de valor limitado para os administradores do sistema.

Um evento intrínseco é representado por uma instância de uma classe derivada de \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent ou \_ \_ ClassOperationEvent. Todas as alterações nas instâncias no WMI são representadas pela classe InstanceOperationEvent e pelas classes derivadas \_ \_ dela: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent e \_ \_ InstanceDeletionEvent.

O monitoramento de recursos usando o WMI envolve instâncias de monitoramento e todas as alterações nas instâncias são representadas por \_ \_ InstanceOperationEvent e as classes derivadas dele. Isso significa que o monitoramento de recursos envolve, em última análise, instâncias de monitoramento de classes derivadas \_ \_ de InstanceOperationEvent.

Você registra o interesse em instâncias de uma dessas classes emindo uma consulta de notificação expressa no WQL. A consulta usa sintaxe semelhante à seguinte:

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Para uma discussão mais longa sobre como usar os eventos de instância WMI para monitorar a atividade do computador, consulte Como posso monitorar diferentes tipos de eventos [com apenas um script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Exemplos

O [exemplo de](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) código VBScript do evento monitorar processo na Galeria do TechNet usa **\_ \_ InstanceOperationEvent** para monitorar o primeiro evento de instância WMI para o Processo [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Escrevendo em um arquivo de log com base em um evento](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

