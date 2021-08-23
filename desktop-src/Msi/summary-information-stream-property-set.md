---
description: A tabela a seguir mostra o conjunto de propriedades fluxo de informações resumidas, que inclui as propriedades, suas IDs de propriedade correspondentes, PIDs e tipos.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Conjunto de propriedades de fluxo de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d41439e15a59ca1942fcbb49c06067251060935b165d6a34972df868fa7feac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627046"
---
# <a name="summary-information-stream-property-set"></a>Conjunto de propriedades de fluxo de informações de resumo

A tabela a seguir mostra o conjunto de propriedades fluxo de informações resumidas, que inclui as propriedades, suas IDs de propriedade correspondentes, PIDs e tipos. Para obter mais informações sobre como o instalador usa essas propriedades, consulte [descrições de propriedades de resumo](summary-property-descriptions.md). Para obter informações sobre as funções do instalador de janela que são usadas para configurar as propriedades de informações de resumo, consulte [usando o fluxo de informações de resumo](using-the-summary-information-stream.md).



| Nome da propriedade                                                | ID da propriedade        | PID | Tipo         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**Código**](codepage-summary.md)                         | \_página de código PID      | 1   | \_I2 VT       |
| [**Título**](title-summary.md)                               | título da PID \_         | 2   | a VT \_ LPSTR    |
| [**Assunto**](subject-summary.md)                           | \_entidade PID       | 3   | a VT \_ LPSTR    |
| [**Autor**](author-summary.md)                             | autor da PID \_        | 4   | a VT \_ LPSTR    |
| [**Palavras-chave**](keywords-summary.md)                         | \_palavras-chave PID      | 5   | a VT \_ LPSTR    |
| [**Comentários**](comments-summary.md)                         | Comentários de PID \_      | 6   | a VT \_ LPSTR    |
| [**Modelo**](template-summary.md)                         | \_modelo PID      | 7   | a VT \_ LPSTR    |
| [**Salvo pela última vez por**](last-saved-by-summary.md)               | DTI \_ LASTAUTHOR    | 8   | a VT \_ LPSTR    |
| [**Número de revisão**](revision-number-summary.md)           | DTI \_ REVNUMBER     | 9   | a VT \_ LPSTR    |
| [**Última Impressão**](last-printed-summary.md)                 | DTI \_ LASTPRINTED   | 11  | FILETIME do VT \_ |
| [**Criar data/hora**](create-time-date-summary.md)         | PID \_ criar \_ DTM   | 12  | FILETIME do VT \_ |
| [**Hora do último salvamento/data**](last-saved-time-date-summary.md)  | DTI \_ LASTSAVE \_ DTM | 13  | FILETIME do VT \_ |
| [**Contagem de páginas**](page-count-summary.md)                     | DTI \_ PageCount     | 14  | \_I4 VT       |
| [**Contagem de palavras**](word-count-summary.md)                     | DTI \_ WORDCOUNT     | 15  | \_I4 VT       |
| [**Contagem de caracteres**](character-count-summary.md)           | DTI \_ charCount     | 16  | \_I4 VT       |
| [**Criando aplicativo**](creating-application-summary.md) | \_APPNAME PID       | 18  | a VT \_ LPSTR    |
| [**Segurança**](security-summary.md)                         | segurança de PID \_      | 19  | \_I4 VT       |



 

Atualmente, o instalador mantém três formatos de armazenamento para pacotes de instalação, transformações e pacotes de patches. O CLSID para o armazenamento é definido como a classe de formato apropriada para o formato específico, independentemente das informações de resumo do armazenamento.

 

 



