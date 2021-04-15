---
description: Identificadores de evento identificam exclusivamente um evento específico.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificadores de evento (log de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502062"
---
# <a name="event-identifiers-event-logging"></a>Identificadores de evento (log de eventos)

Identificadores de evento identificam exclusivamente um evento específico. Cada [origem de evento](event-sources.md) pode definir seus próprios eventos numerados e as cadeias de caracteres de descrição para as quais eles são mapeados em seu arquivo de mensagem. Os visualizadores de eventos podem apresentar essas cadeias de caracteres ao usuário. Eles devem ajudar o usuário a entender o que deu errado e a sugerir as ações a serem tomadas. Direcione a descrição para os usuários que resolvem seus próprios problemas, não para administradores ou técnicos de suporte. Para obter mais informações, consulte [diretrizes de mensagem de erro](/windows/desktop/Debug/error-message-guidelines).

## <a name="format"></a>Formatar

O diagrama a seguir ilustra o formato de um identificador de evento.

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev
</dt> <dd>

Gravidade. A severidade é definida da seguinte maneira:

<dl> <dd>00-êxito</dd> <dd>01-informativo</dd> <dd>10-aviso</dd> <dd>11-erro</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>&
</dt> <dd>

Bit do cliente. Esse bit é definido da seguinte maneira:

<dl> <dd>0-código do sistema</dd> <dd>1-código do cliente</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>D
</dt> <dd>

Bit reservado.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Saldo
</dt> <dd>

Código de instalação. Esse valor pode ser um recurso \_ nulo.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
</dt> <dd>

Código de status para a instalação.

</dd> </dl>

## <a name="message-definitions"></a>Definições de mensagem

As mensagens são definidas no arquivo de mensagem de evento. As cadeias de caracteres de descrição no arquivo de mensagem de evento são indexadas pelo identificador de evento, permitindo que Visualizador de Eventos exiba texto específico de evento para qualquer evento com base no identificador de evento. Todas as descrições são localizadas e dependentes do idioma. Para obter mais informações sobre como criar um arquivo de mensagem, consulte [arquivos de texto da mensagem](message-text-files.md).

As cadeias de caracteres de descrição podem conter espaços reservados de cadeia de inserção, do formato%*n*, onde %1 indica a primeira cadeia de caracteres de inserção e assim por diante. Por exemplo, veja a seguir um exemplo de entrada no arquivo. MC:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

Nesse caso, o buffer retornado por [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contém cadeias de caracteres de inserção. O membro **NumStrings** da estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica o número de cadeias de caracteres de inserção. O membro **StringOffset** da estrutura **EVENTLOGRECORD** indica o local da primeira cadeia de caracteres de inserção no buffer. Você pode passar uma matriz de \_ Ptrs DWORD que aponta para o endereço de cada cadeia de caracteres no buffer ao chamar a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e irá inserir as cadeias de caracteres na mensagem.

A cadeia de caracteres de descrição também pode conter espaços reservados para cadeias de caracteres de parâmetro do arquivo de mensagem de parâmetro. Os espaços reservados estão no formato%%*n*, onde% %1 é substituído pela cadeia de caracteres do parâmetro com o identificador de 1 e assim por diante. No entanto, cabe a você inserir as cadeias de caracteres de parâmetro na cadeia de mensagem que [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) retorna. Normalmente, você chama **FormatMessage** para obter a cadeia de caracteres da mensagem para o evento. Em seguida, analise a cadeia de caracteres da mensagem para%%*n* parâmetros. Se a mensagem contiver um ou mais parâmetros, carregue o valor do registro **ParameterMessageFile** para a origem. Para cada parâmetro na cadeia de caracteres de mensagem, obtenha o identificador e passe-o para **FormatMessage** para obter a cadeia de caracteres do parâmetro. Substitua o parâmetro na cadeia de caracteres de mensagem pela cadeia de caracteres de parâmetro retornada por **FormatMessage** .

## <a name="insertion-strings"></a>Cadeias de caracteres de inserção

Cadeias de caracteres de inserção são cadeias de caracteres opcionais independentes de idioma usadas para preencher valores para espaços reservados em cadeias de caracteres de descrição. Como as cadeias de caracteres não são localizadas, é essencial que esses espaços reservados sejam usados apenas para representar cadeias de caracteres independentes de idioma, como valores numéricos, nomes de arquivos, nomes de usuário e assim por diante. O comprimento da cadeia de caracteres não deve exceder 32 quilobytes-1 caracteres.

Evite usar várias cadeias de caracteres para criar uma descrição maior. Uma cadeia de caracteres de inserção deve ser tratada como dados, não texto. Por exemplo, no exemplo a seguir, pszString1 e pszString2 não devem ser usados como cadeias de caracteres de inserção para pszDescription.

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

No exemplo a seguir, é apropriado usar pszString1 ou pszString2 para a cadeia de caracteres de inserção em pszDescription.

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
