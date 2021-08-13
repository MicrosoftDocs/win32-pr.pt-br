---
description: A classe NTEventLogEventConsumer registra uma mensagem específica no log de eventos do sistema operacional quando um evento é entregue a ele.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Classe NTEventLogEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dfa2a1dcf15b65808af758820604df6aa62d7bc59d4e1c69e8d4d6e06b1d93a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555166"
---
# <a name="nteventlogeventconsumer-class"></a>Classe NTEventLogEventConsumer

A **classe NTEventLogEventConsumer** registra uma mensagem específica no log de eventos do sistema operacional quando um evento é entregue a ele. Essa classe é um dos consumidores de eventos padrão que o WMI fornece. Para obter mais informações, [consulte Monitoramento e resposta a eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a>Membros

A **classe NTEventLogEventConsumer** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe NTEventLogEventConsumer** tem essas propriedades.

<dl> <dt>

**Categoria**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Categoria de evento. Essas são informações específicas da origem e podem ter qualquer valor.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro. O WMI armazena o SID do usuário que cria uma instância do [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do Administrador, dependendo do sistema operacional. Para obter mais informações, consulte [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).

Essa propriedade é herdada [**\_ \_ de EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Mensagem de evento na DLL da mensagem. Essa propriedade não pode ser **NULL.**

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de evento. Esse parâmetro pode ter um dos valores listados na lista a seguir, que são definidos em Winnt.h.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG \_ SUCCESS** (0 (0x0))


</dt> <dd>

Evento bem-sucedido

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG \_ ERRO \_ TPYE** (1 (0x1))


</dt> <dd>

Evento de erro

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG \_ TIPO \_ DE** AVISO (2 (0x2))


</dt> <dd>

Evento de aviso

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG \_ TIPO \_ DE** INFORMAÇÃO (4 (0x4))


</dt> <dd>

Evento de informações

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG \_ AUDIT \_ SUCCESS** (8 (0x8))


</dt> <dd>

Tipo de auditoria bem-sucedido

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG \_ AUDIT \_ FAILURE** (16 (0x10))


</dt> <dd>

Tipo de auditoria de falha

</dd> </dl>

</dd> <dt>

**InsertionStringTemplates**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de modelos de cadeia de caracteres padrão que é usada como a cadeia de caracteres de inserção para um registro de log de eventos.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do computador para o qual Windows WMI (Instrumentação de Gerenciamento) envia eventos.

Essa propriedade é herdada [**\_ \_ de EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Maximumqueuesize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fila máxima para um consumidor específico, em bytes.

Essa propriedade é herdada [**\_ \_ de EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](key-qualifier.md)
</dt> </dl>

Nome exclusivo de um consumidor.

</dd> <dt>

**NameOfRawDataProperty**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da propriedade de evento que contém os dados a serem passados para o parâmetro *lpRawData* da função [**ReportEvent.**](/windows/desktop/api/winbase/nf-winbase-reporteventa)

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da propriedade de evento que contém um SID (identificador de segurança) a ser passado para o parâmetro *lpUserSid* da função [**ReportEvent.**](/windows/desktop/api/winbase/nf-winbase-reporteventa) A propriedade deve ser uma matriz de bytes (**uint8**) ou uma cadeia de caracteres. Se for uma matriz de bytes, supõe-se que seja um SID. Se for uma cadeia de caracteres, será um SID de cadeia de caracteres convertido em um SID.

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de elementos na **matriz InsertionStringTemplates.**

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da origem em que uma mensagem está localizada. Supõe-se que o cliente tenha registrado uma DLL com as mensagens necessárias.

> [!Note]  
> O valor desse parâmetro não deve incluir dois-pontos (:) Caractere.

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do computador no qual registrar um evento ou **NULL** se o evento deve ser registrado em um servidor local.

Os usuários autenticados não podem, por padrão, registrar eventos no log do aplicativo em um computador remoto. Como resultado, o uso dessa propriedade para especificar um computador remoto não funcionará. Para saber como alterar a segurança do log de eventos, consulte este [artigo da KB](https://support.microsoft.com/kb/323076).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe NTEventLogEventConsumer** é derivada da [**\_ \_ classe abstrata EventConsumer.**](--eventconsumer.md)

## <a name="examples"></a>Exemplos

Para ver um exemplo de como **usar NTEventLogEventConsumer** para criar um consumidor, consulte Registro em log no log de eventos [do NT com base em um evento](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Assinatura \\ raiz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de consumidor padrão](standard-consumer-classes.md)
</dt> <dt>

[Criando um consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

