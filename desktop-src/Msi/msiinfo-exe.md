---
description: Msiinfo.exe é um utilitário de linha de comando que usa funções de banco de dados e funções de instalador para editar ou exibir o fluxo de informações de Resumo de um banco de dados.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57487406533b060d9343d4afbdf7e5254c32e15149bb3385f81cc7dc3923fc71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628092"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe é um utilitário de linha de comando que usa [funções de banco de dados](database-functions.md) e funções de [instalador](installer-functions.md) para editar ou exibir o fluxo de [informações de resumo](summary-information-stream.md) de um banco de dados.

## <a name="syntax"></a>Syntax

**MsiInfo** *{Database} \[ \[ /b \] /d \] {opção} {Data}*

-   O banco de dados não pode ser um banco de dados somente leitura.
-   Se nenhum dado seguir uma opção, a propriedade correspondente será removida.
-   Um máximo de 20 opções pode ser especificado na linha de comando. As mesmas propriedades podem ser especificadas várias vezes.
-   Se os dados contiverem um espaço, coloque os dados com aspas. Por exemplo, como/T "meu título".

## <a name="command-line-options"></a>Opções de linha de comando

Msiinfo.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas. Um delimitador de barra também pode ser usado no lugar de um traço. Para obter mais informações, consulte [Summary Information Stream Property Set](summary-information-stream-property-set.md).



| Opção | Descrição                                                                                                                                                                                                                                                                                                                                                      | ID da propriedade        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *nenhum* | Se nenhuma opção for especificada, o utilitário exibirá os valores atuais das propriedades de informações de resumo.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Exibe informações sobre todas as cadeias de caracteres no pool de cadeias de caracteres. A opção-b será válida somente se-d também for usado e-b deverá vir antes da opção-d.                                                                                                                                                                                                                 |                    |     |
| -d     | Exibe informações sobre o pool de cadeias de caracteres. Valida o pool de cadeias de caracteres e fornece informações sobre a página de código do banco de dados. Observe que a página de código do banco de dados é diferente da página de código do fluxo de informações de resumo ( \_ código de página PID). Essa opção também verifica todas as cadeias de caracteres que são inválidas na página de código do banco de dados. |                    |     |
| -i     | Não aplicável. Reservado.                                                                                                                                                                                                                                                                                                                                        | \_dicionário PID    | 0   |
| -c     | Define a [**propriedade de resumo CodePage**](codepage-summary.md).                                                                                                                                                                                                                                                                                                  | \_página de código PID      | 1   |
| -T     | Define a [**propriedade de resumo do título**](title-summary.md).                                                                                                                                                                                                                                                                                                        | título da PID \_         | 2   |
| -j     | Define a [**propriedade de resumo da entidade**](subject-summary.md).                                                                                                                                                                                                                                                                                                    | entidade PID da ID \_    | 3   |
| -a     | Define a [**propriedade de resumo do autor**](author-summary.md).                                                                                                                                                                                                                                                                                                      | autor da PID \_        | 4   |
| -k     | Define a [**propriedade de resumo das palavras-chave**](keywords-summary.md).                                                                                                                                                                                                                                                                                                  | \_palavras-chave PID      | 5   |
| -o     | Define a [**propriedade de Resumo de comentários**](comments-summary.md).                                                                                                                                                                                                                                                                                                  | Comentários de PID \_      | 6   |
| -p     | Define a [**propriedade de resumo do modelo**](template-summary.md).                                                                                                                                                                                                                                                                                                  | \_modelo PID      | 7   |
| -l     | Define a [**última propriedade de resumo salva por Summary**](last-saved-by-summary.md).                                                                                                                                                                                                                                                                                        | DTI \_ LASTAUTHOR    | 8   |
| -v     | Define a [**propriedade de resumo do número de revisão**](revision-number-summary.md).                                                                                                                                                                                                                                                                                    | DTI \_ REVNUMBER     | 9   |
| -E     | Não aplicável. Reservado.                                                                                                                                                                                                                                                                                                                                        | PID \_ EditTime      | 10  |
| -S     | Define a [**última propriedade de resumo impressa**](last-printed-summary.md). Para especificar o ano, o mês, o dia, a hora, o minuto e o segundo, use o formato "aaaa/mm/dd hh: mm: SS." Por exemplo, "1997/06/20 03:25:59".                                                                                                                                                     | DTI \_ LASTPRINTED   | 11  |
| -r     | Define a [**propriedade de resumo da data/hora de criação**](create-time-date-summary.md). Para especificar o ano, o mês, o dia, a hora, o minuto e o segundo, use o formato "aaaa/mm/dd hh: mm: SS." Por exemplo, "1997/06/20 03:25:59".                                                                                                                                             | PID \_ criar \_ DTM   | 12  |
| -Q     | Define a [**última propriedade de Resumo de hora/data salva**](last-saved-time-date-summary.md). Para especificar o ano, o mês, o dia, a hora, o minuto e o segundo, use o formato "aaaa/mm/dd hh: mm: SS." Por exemplo, "1997/06/20 03:25:59".                                                                                                                                     | DTI \_ LASTSAVE \_ DTM | 13  |
| -g     | Define a [**propriedade de Resumo de contagem de páginas**](page-count-summary.md).                                                                                                                                                                                                                                                                                              | DTI \_ PageCount     | 14  |
| -w     | Define a [**propriedade de Resumo de contagem de palavras**](word-count-summary.md).                                                                                                                                                                                                                                                                                              | DTI \_ WORDCOUNT     | 15  |
| -H     | Define a [**propriedade de resumo contagem de caracteres**](character-count-summary.md).                                                                                                                                                                                                                                                                                    | DTI \_ charCount     | 16  |
|        | Não aplicável. Reservado.                                                                                                                                                                                                                                                                                                                                        | miniatura de PID \_     | 17  |
| -n     | Define a [**propriedade de resumo do aplicativo de criação**](creating-application-summary.md).                                                                                                                                                                                                                                                                          | \_APPNAME PID       | 18  |
| -U     | Define a [**propriedade de Resumo de segurança**](security-summary.md).                                                                                                                                                                                                                                                                                                  | segurança de PID \_      | 19  |



 

essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



