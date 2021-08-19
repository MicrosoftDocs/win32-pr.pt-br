---
description: Um arquivo de arquivo de texto para um Windows do Instalador de Texto carrega uma extensão de nome de arquivo .idt.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato de arquivo morto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72c7fe21b547bb5469af00dc9202d90dba3873a7ed86a6db6261a4228097a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145829"
---
# <a name="archive-file-format"></a>Formato de arquivo morto

Um [arquivo de arquivo de texto](text-archive-files.md) para um Windows do Instalador de Texto carrega uma extensão de nome de arquivo .idt. Quando um banco de dados inteiro é exportado para arquivos de arquivo morto, cada tabela no banco de dados tem um arquivo .idt separado. Se uma tabela contiver uma coluna de fluxo, cada fluxo na tabela será representado por um arquivo com uma extensão de nome de arquivo .ibd. Os arquivos .ibd são armazenados em uma pasta com o mesmo nome que a tabela.

## <a name="idt-file-format"></a>Formato de arquivo .idt

O arquivo .idt de uma tabela de banco de dados exportada que contém apenas caracteres ASCII tem o seguinte formato básico.

-   A primeira linha contém os nomes de coluna de tabela separados por guias.
-   A segunda linha contém as definições de coluna separadas por guias.
-   Se o arquivo contém apenas dados ASCII, a terceira linha é nome da tabela e nomes de coluna de chave primária separados por guias.
-   As linhas restantes no arquivo representam linhas na tabela, com colunas separadas por guias.

> [!Note]  
> Se o arquivo contiver dados não ASCII, a terceira linha será a página de código numérico seguida pelo nome da tabela e nomes de coluna de chave primária separados por guias. Um arquivo .idt que contém informações não ASCII deve ser salvo no formato ASCII. Por exemplo, um arquivo de arquivo de texto pode conter os nomes de coluna e tabela codificados como UTF-8, mas o próprio arquivo de arquivo deve ser ASCII. Consulte a seção [Dados ASCII em Arquivos de Arquivo de Texto](ascii-data-in-text-archive-files.md).

 

> [!Note]  
> Os arquivos .idt [ \_ ForceCodepage](-forcecodepage.md) [ \_ e SummaryInformation](-summaryinformation.md) especiais usam formatos estendidos. Consulte as \_ seções ForceCodepage \_ e SummaryInformation para ver descrições de seus formatos.

 

## <a name="column-definitions"></a>Definições de coluna

As definições de coluna são indicadas por caracteres.

-   O primeiro caractere indica o tipo de coluna. Uma letra minúscula indica uma coluna não anulada e uma letra maiúscula indica que a coluna pode conter valores nulos.

    | Caractere | Significado                   |
    |-----------|---------------------------|
    | s, S      | Coluna de cadeia de caracteres             |
    | l, L      | Coluna de cadeia de caracteres localizável |
    | v, V      | Coluna binária             |
    | i, I      | Coluna Integer            |

    

     

-   O segundo caractere indica o tamanho dos dados da coluna.

    > [!Note]  
    > O Windows instalador não usa o tamanho da coluna especificado para limitar o tamanho da cadeia de caracteres que pode ser inserida em um campo de coluna de cadeia de caracteres. No entanto, algumas ferramentas de autor usam o tamanho da coluna especificado para limitar o tamanho de uma cadeia de caracteres válida. É recomendável que as cadeias de caracteres inseridas em qualquer coluna atendem ao requisito de tamanho especificado.

     

    

    | Definição de coluna | Significado                                    |
    |-------------------|--------------------------------------------|
    | s255              | Coluna de cadeia de caracteres não anulada 255 long        |
    | L50               | Coluna de cadeia de caracteres localizável anulada 50 long |
    | i2, I2            | Coluna de inteiro curto                       |
    | i4, I4            | Coluna de inteiro longo                        |

    

     

## <a name="control-character-translation"></a>Controlar conversão de caracteres

Exportar uma tabela para um arquivo de arquivo de texto converte os caracteres de controle para evitar conflitos com delimitadores de arquivo. Durante a escrita no arquivo .idt, os caracteres de controle são traduzidos da seguinte forma.



| Caractere de controle | Tradução em .idt | Significado         |
|-------------------|---------------------|-----------------|
| NULO              | 21                  | Nulo            |
| BS                | 27                  | Espaço de retorno      |
| HT                | 16                  | Tab             |
| Se                | 25                  | Alimentação de linha       |
| FF                | 24                  | Feed de formulário       |
| CR                | 17                  | Retorno de carro |



 

 

 



