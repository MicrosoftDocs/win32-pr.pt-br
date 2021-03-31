---
description: Relata um evento de modificação de namespace, que é um tipo de evento intrínseco que é gerado quando um namespace é modificado.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: Classe __NamespaceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663136"
---
# <a name="__namespacemodificationevent-class"></a>\_\_Classe NamespaceModificationEvent

A classe de sistema **\_ \_ NamespaceModificationEvent** relata um evento de modificação de namespace, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que é gerado quando um namespace é modificado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ NamespaceModificationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ NamespaceModificationEvent** tem essas propriedades.

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ namespace**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cópia da versão original de uma instância de [**\_ \_ namespace**](--namespace.md) . A propriedade **Name** dessa instância identifica o namespace que é modificado.

</dd> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

</dd> <dt>

**\_descritor de segurança** 
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor que o provedor de eventos usa para determinar os usuários que podem receber um evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

> [!Note]  
> Uma  ACL (lista de controle de acesso) nula [**no \_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado a todas as pessoas o tempo todo. Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ namespace**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cópia da instância de [**\_ \_ namespace**](--namespace.md) que é modificada. A propriedade **Name** da instância do **\_ \_ namespace** indica o namespace que é modificado. Essa propriedade é herdada da classe [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que um evento é gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ NamespaceModificationEvent** é derivada de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

As únicas diferenças entre o namespace de destino e o namespace anterior são os qualificadores e propriedades, exceto [**Name**](--namespace.md).

Observe que a propriedade [**Name**](--namespace.md) de uma instância de **\_ \_ namespace** não pode ser alterada porque namespaces não podem ser renomeados. Para modificar o nome de um namespace, a instância do **\_ \_ namespace** deve ser excluída e recriada com um novo nome. Portanto, os eventos de modificação de namespace são gerados quando uma alteração ocorre em qualificadores e propriedades diferentes de **Name**. Um evento de modificação de namespace não é gerado quando ocorre algum tipo de alteração no namespace. Um evento de modificação de namespace é gerado somente quando uma instância de namespace é modificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

