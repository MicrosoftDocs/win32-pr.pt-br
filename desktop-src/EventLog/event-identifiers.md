---
description: Os identificadores de evento identificam exclusivamente um evento específico.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificadores de evento (log de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933ef3fafe77a2d0fbc2e62b5b11dd499eb850dc5cb6b2ecdc6c952fe1a3f205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951435"
---
# <a name="event-identifiers-event-logging"></a>Identificadores de evento (log de eventos)

Os identificadores de evento identificam exclusivamente um evento específico. Cada [origem de](event-sources.md) evento pode definir seus próprios eventos numerados e as cadeias de caracteres de descrição para as quais são mapeadas em seu arquivo de mensagem. Os visualizadores de eventos podem apresentar essas cadeias de caracteres ao usuário. Eles devem ajudar o usuário a entender o que deu errado e sugerir quais ações devem ser tomadas. Direcionar a descrição para os usuários que resolvem seus próprios problemas, não em administradores ou técnicos de suporte. Para obter mais informações, consulte [Diretrizes de mensagem de erro](/windows/desktop/Debug/error-message-guidelines).

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

Gravidade. A severidade é definida da seguinte forma:

<dl> <dd>00 – Êxito</dd> <dd>01 – Informacional</dd> <dd>10 – Aviso</dd> <dd>11 – Erro</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>C
</dt> <dd>

Bit do cliente. Esse bit é definido da seguinte forma:

<dl> <dd>0 – Código do sistema</dd> <dd>1 – Código do cliente</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Bit reservado.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Instalação
</dt> <dd>

Código do recurso. Esse valor pode ser FACILITY \_ NULL.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
</dt> <dd>

Código de status para o recurso.

</dd> </dl>

## <a name="message-definitions"></a>Definições de mensagem

As mensagens são definidas no arquivo de mensagem de evento. As cadeias de caracteres de descrição no arquivo de mensagem de evento são indexadas pelo identificador de evento, permitindo Visualizador de Eventos exibir texto específico do evento para qualquer evento com base no identificador de evento. Todas as descrições são localizadas e dependem do idioma. Para obter mais informações sobre como criar um arquivo de mensagem, consulte [Arquivos de Texto da Mensagem](message-text-files.md).

As cadeias de caracteres de descrição podem conter os espaço reservados da cadeia de caracteres de inserção, do formato %*n,* em que %1 indica a primeira cadeia de caracteres de inserção e assim por diante. Por exemplo, o seguinte é uma entrada de exemplo no arquivo .mc:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

Nesse caso, o buffer retornado por [**ReadEventLog contém**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) cadeias de caracteres de inserção. O **membro NumStrings** da estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica o número de cadeias de caracteres de inserção. O **membro StringOffset** da estrutura **EVENTLOGRECORD** indica o local da primeira cadeia de caracteres de inserção no buffer. Você pode passar uma matriz de PTRs DWORD que apontam para o endereço de cada cadeia de caracteres no buffer ao chamar a \_ [**função FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e ela inserirá as cadeias de caracteres na mensagem.

A cadeia de caracteres de descrição também pode conter os espaço reservados para cadeias de caracteres de parâmetro do arquivo de mensagem de parâmetro. Os espaço reservados são do formato %%*n,* em que %%1 é substituído pela cadeia de caracteres de parâmetro pelo identificador de 1 e assim por diante. No entanto, é responsabilidade você inserir as cadeias de caracteres de parâmetro na cadeia de caracteres de mensagem [**retornada por FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) Normalmente, você chama **FormatMessage para** obter a cadeia de caracteres de mensagem para o evento. Em seguida, você analisará a cadeia de caracteres de mensagem para os parâmetros %%*n.* Se a mensagem contiver um ou mais parâmetros, carregue o valor do Registro **ParameterMessageFile** para a origem. Para cada parâmetro na cadeia de caracteres de mensagem, obter o identificador e passá-lo para **FormatMessage** para obter a cadeia de caracteres de parâmetro. Substitua o parâmetro na cadeia de caracteres de mensagem pela cadeia de caracteres de parâmetro **que FormatMessage retornou.**

## <a name="insertion-strings"></a>Cadeias de caracteres de inserção

Cadeias de caracteres de inserção são cadeias de caracteres opcionais independentes de idioma usadas para preencher valores de espaço reservados em cadeias de caracteres de descrição. Como as cadeias de caracteres não são localizadas, é essencial que esses espaço reservados sejam usados apenas para representar cadeias de caracteres independentes de idioma, como valores numéricos, nomes de arquivo, nomes de usuário e assim por diante. O comprimento da cadeia de caracteres não deve exceder 32 quilobytes - 1 caracteres.

Evite usar várias cadeias de caracteres para criar uma descrição maior. Uma cadeia de caracteres de inserção deve ser tratada como dados, não como texto. Por exemplo, no exemplo a seguir, pszString1 e pszString2 não devem ser usados como cadeias de caracteres de inserção para pszDescription.

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

 

 
