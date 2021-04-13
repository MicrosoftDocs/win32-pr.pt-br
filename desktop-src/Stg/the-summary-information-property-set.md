---
title: O conjunto de propriedades de informações de resumo
description: COM define um conjunto de propriedades comuns padrão para armazenar informações de resumo sobre documentos.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb318daba7e0ad03ff176853877fe416ddeda799
ms.sourcegitcommit: fc240ac77d4c40a9f3a27714d7b852abbd234774
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2019
ms.locfileid: "104364526"
---
# <a name="the-summary-information-property-set"></a>O conjunto de propriedades de informações de resumo

COM define um conjunto de propriedades comuns padrão para armazenar informações de resumo sobre documentos. O conjunto de propriedades de informações de resumo deve ser armazenado em um objeto de fluxo. Ou seja, esse conjunto de propriedades deve ser armazenado como um conjunto de propriedades simples. Para obter mais informações, consulte [armazenamento e objetos de fluxo para um conjunto de propriedades](storage-vs--stream-for-a-property-set.md).

Por exemplo, para criar um conjunto de propriedades simples ANSI, você chamaria [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) para criar o conjunto de propriedades, especificando **PROPSETFLAG \_ ANSI** (Simple é o tipo padrão de Property Set) e, em seguida, gravará nele com uma chamada para [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Para ler o conjunto de propriedades, você chamaria [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple).

Todos os conjuntos de propriedades compartilhadas são identificados por um fluxo ou nome de armazenamento com o prefixo " \\ 005" (ou 0x05) para mostrar que é um conjunto de propriedades que pode ser compartilhado entre aplicativos. O conjunto de propriedades de informações de resumo não é exceção. O nome do fluxo que contém o conjunto de propriedades de informações de resumo é: **" \\ 005SummaryInformation"**

Não é necessário saber o nome do fluxo do conjunto de propriedades ao acessá-lo por meio dos métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) da interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ; Nesse caso, somente o identificador de formato (FMTID) precisa ser conhecido. O FMTID para o conjunto de propriedades de informações de resumo é: **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

A declaração para esse valor está disponível no arquivo de cabeçalho como **FMTID \_ SummaryInformation**. Para obter mais informações, consulte o FMTIDS nos [identificadores de formato do conjunto de propriedades predefinidas](predefined-property-set-format-identifiers.md).

A tabela a seguir lista os nomes de propriedade de cadeia de caracteres para o conjunto de propriedades de informações de resumo, juntamente com os respectivos identificadores de propriedade e indicadores de tipo de variável (VT). Os nomes normalmente não são armazenados no conjunto de propriedades, mas são inferidos do valor de ID de propriedade. As entradas de cadeia de caracteres de ID de propriedade mostradas aqui correspondem às definições encontradas nos arquivos de cabeçalho.

| Nome | Cadeia de caracteres de ID de propriedade | ID da propriedade | Tipo VT |
|------|--------------------|-------------|---------|
| Título | título do PIDSI \_ | 0x00000002 | a VT \_ LPSTR  |
| Assunto | assunto do PIDSI \_ | 0x00000003 | a VT \_ LPSTR |
| Autor | autor do PIDSI \_ | 0x00000004 | a VT \_ LPSTR |
| Palavras-chave | \_palavras-chave PIDSI | 0x00000005 | a VT \_ LPSTR |
| Comentários | PIDSI \_ comentários | 0x00000006 | a VT \_ LPSTR |
| Modelo | \_modelo PIDSI | 0x00000007 | a VT \_ LPSTR |
| Salvo pela última vez por | PIDSI \_ LASTAUTHOR | 0x00000008 | a VT \_ LPSTR |
| Número de Revisão | PIDSI \_ REVNUMBER | 0x00000009 | a VT \_ LPSTR |
| Tempo total de edição | PIDSI \_ EditTime | 0x0000000A | VT \_ FILETIME (UTC) |
| Última Impressão | PIDSI \_ LASTPRINTED | 0x0000000B | VT \_ FILETIME (UTC) |
| Criar data/hora (veja a observação abaixo) | PIDSI \_ criar \_ DTM | 0x0000000C | VT \_ FILETIME (UTC) |
| Hora da última gravação/data (consulte a observação abaixo) | PIDSI \_ LASTSAVE \_ DTM | 0x0000000D | VT \_ FILETIME (UTC) |
| Número de páginas | PIDSI \_ PageCount | 0x0000000E | \_I4 VT |
| Número de palavras | PIDSI \_ WORDCOUNT | 0x0000000F | \_I4 VT |
| Número de Caracteres | PIDSI \_ charCount | 0x00000010 | \_I4 VT |
| Thumbnail | miniatura de PIDSI \_ | 0x00000011 | VT \_ CF |
| Nome da criação do aplicativo | \_APPNAME PIDSI | 0x00000012 | a VT \_ LPSTR |
| Segurança | segurança do PIDSI \_ | 0x00000013 | \_I4 VT |

> [!NOTE]
> Para **criar hora/data** e **hora/data da última gravação**, alguns métodos de transferência de arquivo, como um download de um BBS, não mantêm corretamente a versão do sistema de arquivos dessas informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementando o conjunto de propriedades de informações de resumo](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




