---
description: Quando uma tabela que contém apenas caracteres ASCII é exportada para um arquivo morto de texto, o arquivo. IDT segue o formato de arquivo morto básico.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Dados ASCII em arquivos mortos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7fa327d19b59793862bd2c06ce814b17979e8e8a6f72d41b1af677b715b4ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078066"
---
# <a name="ascii-data-in-text-archive-files"></a>Dados ASCII em arquivos mortos de texto

Quando uma tabela que contém apenas caracteres ASCII é exportada para um [arquivo morto de texto](text-archive-files.md), o arquivo. IDT segue o [formato de arquivo morto](archive-file-format.md)básico. Se a tabela contiver informações não ASCII, o formato do arquivo morto será estendido para incluir informações de página de código.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>Arquivos mortos de texto que contêm apenas caracteres ASCII

Quando uma tabela que contém apenas caracteres ASCII é exportada para um arquivo morto, o arquivo. IDT está no [formato básico de arquivo morto](archive-file-format.md). Cada fluxo na tabela é exportado como um arquivo com uma extensão de nome de arquivo. IBD. Os arquivos. IBD são armazenados em uma pasta com o mesmo nome que a tabela. Por exemplo, considere a exportação da tabela [binária](binary-table.md) a seguir.



| Nome  | Dados      |
|-------|-----------|
| Manuais | Books. IBD |
| Cars  | Carros. IBD  |



 

A estrutura de diretório depois de exportar essa tabela é a seguinte. As informações na tabela de banco de dados são exportadas para Binary. IDT. Os dois fluxos de dados binários são exportados para book. IBD e carros. IBD salvos na pasta denominada Binary.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

O arquivo morto Binary. IDT está no formato básico de [arquivo morto](archive-file-format.md) e teria a seguinte aparência.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>Arquivos mortos de texto que contêm caracteres não ASCII

Se o arquivo contiver dados não ASCII, o [formato de arquivo morto](archive-file-format.md) básico do arquivo. IDT será estendido para incluir informações de página de código. A terceira linha na tabela. IDT é a página de código numérica seguida pelo nome da tabela e nomes de coluna de chave primária separados por guias.

> [!Note]  
> Um arquivo. IDT que contém informações não ASCII deve ser salvo no formato ASCII. Por exemplo, um arquivo morto de texto pode conter os nomes de coluna e tabela codificados como UTF-8, mas o arquivo morto em si deve ser ASCII.

 

A seguinte tabela ActionText localizada em francês conterá informações não ASCII. A página de código numérico usada para cadeias de caracteres francesas é 1252.



| Ação    | Descrição                                  | Modelo |
|-----------|----------------------------------------------|----------|
| ANUNCIAR | Publicação d'informations sur l'application |          |



 

O arquivo morto exportado, ActionText. IDT, seria o seguinte.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Se um arquivo morto de texto contiver dados não ASCII, o arquivo morto incluirá informações de página de código. Arquivos mortos com informações de página de código só podem ser importados de volta para um banco de dados dessa página de código exata ou para um banco de dados neutro de idioma. No caso de um banco de dados com neutralidade de idioma, a página de código é definida como a página de código do arquivo morto. para obter mais informações sobre como Windows Installer manipula páginas de código, consulte a seção [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).

 

 

 



