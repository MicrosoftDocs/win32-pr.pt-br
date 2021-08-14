---
description: A classe LogFileEventConsumer grava cadeias de caracteres personalizadas em um arquivo de log de texto quando os eventos são entregues a ele.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Classe LogFileEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dbcf0f90a8bca0cf1f648f74d1b58d7037b79fa8bc9d2d13c4fe2c6dc8306eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996516"
---
# <a name="logfileeventconsumer-class"></a>Classe LogFileEventConsumer

A **classe LogFileEventConsumer** grava cadeias de caracteres personalizadas em um arquivo de log de texto quando os eventos são entregues a ele. As cadeias de caracteres são separadas por sequências de fim de linha. Essa classe é um dos consumidores de eventos padrão que o WMI fornece. Para obter mais informações, [consulte Monitoramento e resposta a eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a>Membros

A **classe LogFileEventConsumer** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe LogFileEventConsumer** tem essas propriedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro. O WMI armazena o SID do usuário que cria uma instância do [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do Administrador, dependendo do sistema operacional. Para obter mais informações, consulte [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).

Essa propriedade é herdada [**\_ \_ de EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Filename**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de um arquivo que inclui o caminho ao qual as entradas de log são anexadas. Se o arquivo não existir, **LogFileEventConsumer** tentará crie-o. O consumidor falha quando o caminho não existe ou quando o usuário que cria o consumidor não tem permissões de gravação para o arquivo ou caminho.

</dd> <dt>

**IsUnicode**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, o arquivo de log será um arquivo de texto Unicode. Se **FALSE**, o arquivo de log será um arquivo de texto de código multibyte. Se o arquivo existir, essa propriedade será ignorada e a configuração de arquivo atual será usada. Por exemplo, se **IsUnicode** for **FALSE,** mas o arquivo existente for um arquivo Unicode, Unicode será usado. Se **IsUnicode** for **TRUE,** mas o arquivo for um código multibyte, o código multibyte será usado.

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

**Maximumfilesize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho máximo de um arquivo de log em bytes. Se o arquivo primário exceder seu tamanho máximo, o conteúdo será movido para um arquivo diferente e o arquivo primário será esvaziado. Um valor de 0 (zero) significa que não há nenhum limite de tamanho. O valor padrão é 65.535 bytes. O tamanho do arquivo é verificado antes de uma operação de gravação. Portanto, você pode ter um arquivo um pouco maior que o limite de tamanho especificado. A próxima operação de gravação o captura e inicia um novo arquivo.

A lista a seguir identifica a estrutura de nomeação para o arquivo de backup:

-   Se o nome de arquivo original for 8.3, a extensão será substituída por uma cadeia de caracteres no formato "001", "002" e assim por diante com o menor número maior do que todos os números usados anteriormente e escolhidos. Se "999" for usado, o número escolhido será o menor número não utilizado.
-   Se o nome de arquivo original não for 8.3, uma cadeia de caracteres no formato "001", "002" e assim por diante será anexada ao nome do arquivo.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Nome exclusivo para esse consumidor.

</dd> <dt>

**Text**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Modelo de cadeia [de caracteres](using-standard-string-templates.md) padrão para o texto de uma entrada de log.

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O **LogFileEventConsumer** não segura o arquivo de log. Portanto, ao configurar o **LogFileEventConsumer**, é importante especificar um diretório protegido para o nível necessário.

 

A **classe LogFileEventConsumer** é derivada da [**\_ \_ classe abstrata EventConsumer.**](--eventconsumer.md)

## <a name="examples"></a>Exemplos

Para ver um exemplo de **como usar LogFileEventConsumer** para criar um consumidor, consulte Escrevendo em um arquivo de [log com base em um evento](writing-to-a-log-file-based-on-an-event.md).

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

[Escrevendo em um arquivo de log com base em um evento](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Criando um consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

