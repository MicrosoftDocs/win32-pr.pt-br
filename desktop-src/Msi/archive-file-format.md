---
description: Um arquivo morto de texto para um banco de dados Windows Installer transporta uma extensão de nome de arquivo. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato de arquivo morto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828065"
---
# <a name="archive-file-format"></a>Formato de arquivo morto

Um [arquivo morto de texto](text-archive-files.md) para um banco de dados Windows Installer transporta uma extensão de nome de arquivo. IDT. Quando um banco de dados inteiro é exportado para arquivos mortos, cada tabela no banco de dados tem um arquivo. IDT separado. Se uma tabela contiver uma coluna de fluxo, cada fluxo na tabela será representado por um arquivo com uma extensão de nome de arquivo. IBD. Os arquivos. IBD são armazenados em uma pasta com o mesmo nome que a tabela.

## <a name="idt-file-format"></a>Formato de arquivo. IDT

O arquivo. IDT de uma tabela de banco de dados exportada que contém apenas caracteres ASCII tem o seguinte formato básico.

-   A primeira linha contém os nomes de coluna de tabela separados por tabulações.
-   A segunda linha contém as definições de coluna separadas por tabulações.
-   Se o arquivo contiver apenas dados ASCII, a terceira linha será nome da tabela e nomes de coluna de chave primária separados por tabulações.
-   As linhas restantes no arquivo representam linhas na tabela, com colunas separadas por tabulações.

> [!Note]  
> Se o arquivo contiver dados não ASCII, a terceira linha será a página de código numérico seguida pelo nome da tabela e nomes de coluna de chave primária separados por tabulações. Um arquivo. IDT que contém informações não ASCII deve ser salvo no formato ASCII. Por exemplo, um arquivo morto de texto pode conter os nomes de coluna e tabela codificados como UTF-8, mas o arquivo morto em si deve ser ASCII. Consulte a seção [dados ASCII em arquivos mortos de texto](ascii-data-in-text-archive-files.md).

 

> [!Note]  
> Os arquivos especiais [ \_ ForceCodepage](-forcecodepage.md) e [ \_ SummaryInformation](-summaryinformation.md) . IDT usam formatos estendidos. Consulte as \_ seções ForceCodepage e \_ SummaryInformation para obter descrições de seus formatos.

 

## <a name="column-definitions"></a>Definições de coluna

As definições de coluna são indicadas por caracteres.

-   O primeiro caractere indica o tipo de coluna. Uma letra minúscula indica uma coluna não anulável e uma letra maiúscula indica que a coluna pode conter valores nulos.

    | Caractere | Significado                   |
    |-----------|---------------------------|
    | s, S      | Coluna de cadeia de caracteres             |
    | l, L      | Coluna de cadeia de caracteres localizável |
    | v, V      | Coluna binária             |
    | i, I      | Coluna de inteiros            |

    

     

-   O segundo caractere indica o tamanho dos dados da coluna.

    > [!Note]  
    > Na verdade, o Windows Installer não usa o tamanho de coluna especificado para limitar o tamanho da cadeia de caracteres que pode ser inserida em um campo de coluna de cadeia de caracteres. No entanto, algumas ferramentas de criação usam o tamanho de coluna especificado para limitar o tamanho de uma cadeia de caracteres válida. É recomendável que as cadeias de caracteres inseridas em qualquer coluna atendam ao requisito de tamanho especificado.

     

    

    | Definição de coluna | Significado                                    |
    |-------------------|--------------------------------------------|
    | s255              | Coluna de cadeia de caracteres não anulável 255 longo        |
    | L50               | Coluna de cadeia de caracteres localizável inanulável 50 longo |
    | i2, I2            | Coluna de inteiro curto                       |
    | i4, i4            | Coluna de inteiro longo                        |

    

     

## <a name="control-character-translation"></a>Conversão de caracteres de controle

Exportar uma tabela para um arquivo morto de texto traduz os caracteres de controle para evitar conflitos com delimitadores de arquivo. Durante a gravação no arquivo. IDT, os caracteres de controle são traduzidos da seguinte maneira.



| Caractere de controle | Tradução na. IDT | Significado         |
|-------------------|---------------------|-----------------|
| NULO              | 21                  | Nulo            |
| BS                | 27                  | Espaço de fundo      |
| HT                | 16                  | Tab             |
| ALIMENTAÇÃO                | 25                  | Alimentação de linha       |
| FF                | 24                  | Feed de formulário       |
| CR                | 17                  | Retorno de carro |



 

 

 



