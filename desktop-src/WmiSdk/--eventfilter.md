---
description: O registro de um consumidor de evento permanente requer uma instância da \_ \_ classe de sistema EventFilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: Classe __EventFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
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
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763009"
---
# <a name="__eventfilter-class"></a>\_\_Classe EventFilter

O registro de um consumidor de evento permanente requer uma instância da classe de sistema **\_ \_ EventFilter** .

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventFilter** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventFilter** tem essas propriedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

SID (identificador de segurança) que identifica exclusivamente o usuário que cria esse filtro. Instrumentação de gerenciamento do Windows (WMI) armazena o SID do usuário que cria uma instância de **\_ \_ EventFilter** ou o SID do administrador, dependendo do sistema operacional. Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**EventAccess**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Descritor de segurança (SD) na linguagem de definição de descritor de segurança (SDDL) que controla o acesso a eventos entregues ao filtro. Use essa propriedade para especificar que somente os eventos no contexto de segurança de contas específicas podem ser entregues a esse filtro. Por exemplo, um consumidor de evento permanente pode limpar os logs de segurança somente quando um evento específico é gerado por um usuário específico. Para especificar quem pode publicar eventos nesse filtro, use a máscara **de \_ \_ publicação do WBEM direito** na ACE (entrada de controle de acesso) para a propriedade do [**\_ descritor de segurança**](--event.md) . Para obter mais informações, consulte [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](wmi-security-constants.md). Para obter mais informações e exemplos, consulte replace:[recebendo eventos com segurança](receiving-events-securely.md).

Você pode configurar um descritor de segurança de acesso de evento para permitir que um evento seja entregue somente quando a conta do sistema local gerar o evento. Para obter mais informações sobre como criar um descritor de segurança e autorizar o acesso, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).

Exemplo: a cadeia de caracteres SDDL a seguir permite que somente administradores forneçam eventos para o filtro. O direito necessário para fornecer eventos é **a \_ \_ publicação do WBEM à direita** (x80).


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

**EventNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Namespace da instância de evento usada para assinaturas de namespace cruzado.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

Identificador exclusivo de um filtro de eventos. Como um filtro de eventos é usado apenas internamente pelo WMI, é recomendável que você defina essa propriedade como um **GUID**(identificador global exclusivo) convertido em uma cadeia de caracteres. No entanto, os consumidores podem usar qualquer esquema privado para um nome de filtro, contanto que não haja um conflito com outros filtros.

</dd> <dt>

**Consulta**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Consulta de evento WQL (linguagem de consulta Instrumentação de Gerenciamento do Windows) que especifica o conjunto de eventos para notificação do consumidor e as condições específicas para notificação.

</dd> <dt>

**QueryLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Idioma usado para a consulta. Como o WMI atualmente suporta apenas linguagem WQL (WQL) como uma linguagem de consulta, essa propriedade deve ser definida como "WQL".

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ EventFilter** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md).

## <a name="examples"></a>Exemplos

O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **\_ \_ EventFilter** como parte de um script complexo para configurar um registro de evento do WMI permanente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Criando um filtro de eventos](creating-an-event-filter.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[Monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Eventos de monitoramento](monitoring-events.md)
</dt> <dt>

[Classes de consumidor padrão](standard-consumer-classes.md)
</dt> <dt>

[Protegendo eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

