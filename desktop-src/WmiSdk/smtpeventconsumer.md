---
description: A classe SMTPEventConsumer envia uma mensagem de email usando o protocolo SMTP sempre que um evento é entregue a ele.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Classe SMTPEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 4f216647f7ac6796c4b94157a261e535d9e2eb9cd98e02fd1f9cec5ac3dee95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922937"
---
# <a name="smtpeventconsumer-class"></a>Classe SMTPEventConsumer

A classe **SMTPEventConsumer** envia uma mensagem de email usando o protocolo SMTP sempre que um evento é entregue a ele. Um servidor SMTP deve existir na rede. A classe SMTPEventConsumer não dá suporte a anexos. A codificação da mensagem de email deve ser US-ASCII.

Essa classe é um dos consumidores de eventos padrão que o WMI fornece. Para obter um exemplo de como usar o **SMTPEventConsumer** para criar um consumidor, consulte [enviando email com base em um evento](sending-e-mail-based-on-an-event.md). Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a>Membros

A classe **SMTPEventConsumer** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SMTPEventConsumer** tem essas propriedades.

<dl> <dt>

**BccLine**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de endereços, separados por vírgula ou ponto-e-vírgula, no formato de um modelo de cadeia de caracteres padrão ao qual a mensagem é enviada como uma cópia carbono oculta. Para obter mais informações, consulte a seção comentários deste tópico.

</dd> <dt>

**CcLine**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de endereços, separados por vírgula ou ponto-e-vírgula, no formato de um modelo de cadeia de caracteres padrão para o qual a mensagem é enviada como uma cópia carbono. Para obter mais informações, consulte a seção comentários deste tópico.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro. O WMI armazena o SID do usuário que cria uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do administrador, dependendo do sistema operacional. Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**A partir de**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Da linha de uma mensagem de email no formato de um modelo de cadeia de caracteres padrão. Se for **NULL**, uma linha from será construída na forma de "winmgmt@*MachineName*".

</dd> <dt>

**HeaderFields**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de campos de cabeçalho que são inseridos em uma mensagem de email sem interpretação.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.

Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fila máxima para um consumidor específico, em bytes.

Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Modelo de cadeia de caracteres padrão que contém o corpo de uma mensagem de email.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](key-qualifier.md)
</dt> </dl>

Identificador exclusivo para o consumidor do evento.

</dd> <dt>

**ReplyToLine**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Linha de resposta de uma mensagem de email no formato de um modelo de cadeia de caracteres padrão. Se **NULL**, nenhuma linha de resposta será usada.

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do servidor SMTP por meio do qual um email é enviado. Os nomes permitidos são um endereço IP ou um DNS ou um nome NetBIOS. Esta propriedade não pode ser **nula**.

</dd> <dt>

**Assunto**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Modelo de cadeia de caracteres padrão que contém o assunto de uma mensagem de email.

</dd> <dt>

**ToLine**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de endereços, separados por vírgula ou ponto-e-vírgula, no formato de um modelo de cadeia de caracteres padrão que identifica onde a mensagem deve ser enviada. Para obter mais informações, consulte a seção comentários deste tópico.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe SMTPEventConsumer é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) .

Algumas das propriedades **ToLine**, **CcLine** ou **BccLine** podem ser **nulas**, mas elas não podem ser **nulas**.

Receber um código de retorno de erro do serviço SMTP é considerado uma falha.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar o **SMTPEventConsumer** para criar um consumidor, consulte [enviando email com base em um evento](sending-e-mail-based-on-an-event.md). Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Assinatura raiz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[Classes de consumidor padrão](standard-consumer-classes.md)
</dt> <dt>

[Enviando email com base em um evento](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[Criando um consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> </dl>

 

 




