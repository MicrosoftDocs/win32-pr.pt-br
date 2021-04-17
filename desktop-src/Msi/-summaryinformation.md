---
description: A \_ tabela SummaryInformation é uma tabela especial usada com o fluxo de informações de resumo. Você pode obter ou definir o fluxo de informações de Resumo de um banco de dados Windows Installer exportando ou importando um arquivo morto de texto chamado \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749598"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

A \_ tabela SummaryInformation é uma tabela especial usada com o [fluxo de informações de resumo](summary-information-stream.md). Você pode obter ou definir o fluxo de informações de Resumo de um banco de dados Windows Installer exportando ou importando um [arquivo morto de texto](text-archive-files.md) chamado \_ SummaryInformation. IDT.

O arquivo. IDT de uma tabela SummaryInformation exportada \_ tem o formato a seguir.

-   A primeira linha contém os nomes de coluna de tabela separados por tabulações: PropertyId e valor. Consulte o tópico [conjunto de propriedades fluxo de informações de resumo](summary-information-stream-property-set.md) para obter uma lista das propriedades e suas IDs (PID).
-   A segunda linha contém as definições de coluna separadas por tabulações. As definições de coluna são especificadas da mesma maneira que no [formato de arquivo](archive-file-format.md). IDT básico. A coluna PropertyId pode ser um inteiro curto não anulável. A coluna Value pode ser uma cadeia de caracteres 255 de comprimento não anulável.
-   A terceira linha é o nome da tabela e o nome da coluna de chave primária separados por tabulações: \_ SummaryInformation e PropertyId.
-   As linhas restantes no arquivo representam a PID e o valor associado, separados por tabulações. A data e a hora em \_ SummaryInformation estão no formato: aaaa/mm/dd hh:: mm:: SS. Por exemplo, 1999/03/22 15:25:45.

Veja a seguir um exemplo do [fluxo de informações de resumo](summary-information-stream.md) de um banco de dados no formato. IDT.

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

Quando você usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou o método de [importação](database-import.md) do objeto de [**banco de dados**](database-object.md) para importar uma tabela de arquivo de texto chamada \_ SummaryInformation para um banco de dados do instalador, você grava o fluxo "05SummaryInformation" no banco de dados.

 

 



