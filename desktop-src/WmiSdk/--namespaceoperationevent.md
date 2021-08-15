---
description: Uma classe base para todos os eventos intrínsecos relacionados a um namespace.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: __NamespaceOperationEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b5293f97eed0716b3add1d5f06513d556355b157d8e594b1f9e55cb8df6ca7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320618"
---
# <a name="__namespaceoperationevent-class"></a>\_\_Classe NamespaceOperationEvent

A **\_ \_ classe de sistema NamespaceOperationEvent** é uma classe base para todos os eventos intrínsecos relacionados a um namespace.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Membros

A **\_ \_ classe NamespaceOperationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe NamespaceOperationEvent** tem essas propriedades.

<dl> <dt>

**DESCRITOR \_ DE SEGURANÇA**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Essa propriedade é herdada do [**\_ \_ Evento**](--event.md).

</dd> <dt>

**Targetnamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ Namespace**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Namespace afetado pelo evento. Para eventos de criação, esse é o namespace recém-criado. Para eventos de modificação, esse é o namespace alterado. Para eventos de exclusão, esse é o namespace excluído.

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

A **\_ \_ classe NamespaceOperationEvent** é derivada de [**\_ \_ Event**](--event.md).

As instâncias dessa classe não são criadas. O WMI cria instâncias de uma das seguintes classes derivadas dessa classe:

[**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)

[**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md)

[**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)

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
</dt> </dl>

 

