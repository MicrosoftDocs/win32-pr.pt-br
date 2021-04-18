---
description: O caminho lógico é usado para organizar os componentes gerenciados por um gravador em grupos bem definidos.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Caminho lógico de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a591f3eec0e00257740dbbd24ab7c609c53c27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763765"
---
# <a name="logical-pathing-of-components"></a>Caminho lógico de componentes

O [*caminho lógico*](vssgloss-l.md) é usado para organizar os componentes gerenciados por um gravador em grupos bem definidos.

O caminho lógico é análogo na estrutura para o caminho de arquivo tradicional, usando a barra invertida " \\ " para separar elementos no caminho. Ao contrário dos caminhos de arquivo, a raiz de um caminho lógico é **nula**, em vez de " \\ ".

O caminho lógico é expresso como uma cadeia de caracteres terminada em **nulo** e não há nenhuma outra restrição nos caracteres que o caminho pode conter.

O uso mais importante de caminhos lógicos é a definição de [*conjuntos de componentes*](vssgloss-c.md), em que a [*inclusão explícita de componentes*](vssgloss-e.md) em uma operação de backup ou restauração de um componente selecionável requer a inclusão de vários outros componentes ([*subcomponente*](vssgloss-s.md)). O caminho lógico do componente de definição de um conjunto de componentes é um pai para os caminhos lógicos de seus subcomponentes e:

-   Os subcomponentes devem compartilhar como um caminho raiz o caminho lógico do componente selecionável que define o conjunto de componentes.
-   Um caminho raiz **nulo** é válido.
-   O nome do componente selecionável de definição deve ser o primeiro elemento de caminho lógico após o caminho raiz para cada Subcomponente não selecionável do conjunto de componentes.
-   Os conjuntos de componentes podem ser aninhados.
-   A combinação do caminho lógico e do nome do componente deve ser exclusiva em todas as instâncias de uma [*classe de gravador*](vssgloss-w.md).

O exemplo hipotético de um gravador *myWriter* com uma estrutura de caminho lógico definida abaixo ilustra o caminho lógico.



| Nome do Componente | Caminho lógico            | Selecionável para backup |
|----------------|-------------------------|-----------------------|
| Executáveis  | ""                      | N                     |
| "ConfigFiles"  | Executáveis           | N                     |
| "LicenseInfo"  | ""                      | S                     |
| “Segurança”     | ""                      | S                     |
| UserInfo     | “Segurança”              | N                     |
| Certificado | “Segurança”              | N                     |
| "writerData"   | ""                      | S                     |
| Conjunto1         | "writerData"            | N                     |
| Janeiro          | "writerData \\ conjunto1"      | N                     |
| Dez          | "writerData \\ conjunto1"      | N                     |
| Conjunto2         | "writerData"            | N                     |
| Janeiro          | "writerData \\ conjunto2"      | N                     |
| Dez          | "writerData \\ conjunto2"      | N                     |
| Consultá        | "writerData \\ QueryLogs" | N                     |
| Usos        | "writerData"            | S                     |
| Janeiro          | "uso de writerData \\ "     | N                     |
| Dez          | "uso de writerData \\ "     | N                     |



 

Observe que os componentes "executáveis" e "ConfigFile" têm uma relação pai-filho, mas ambos não são selecionáveis. Portanto, eles não formam um conjunto de componentes. Sempre que for feito backup ou restauração *do gravador,* esses dois componentes precisarão ser [*explicitamente incluídos*](vssgloss-e.md) na operação.

O componente "LicenseInfo" é selecionável com nenhum ancestral ou descendente. Ele pode ser incluído explicitamente ou não, em uma operação de backup ou restauração, a critério do solicitante.

O componente "segurança" define um conjunto de componentes simples, que não contém nenhum conjunto de componentes abaixo dele.

O componente "writerData" define um conjunto de componentes, que contém uma coleção complexa de componentes com várias hierarquias de caminho lógico bem definidas abaixo dele.

Um subcomponente, "Usage", é selecionável e define um conjunto de componentes.

Vários componentes têm o mesmo nome e são diferenciados por seus caminhos lógicos. As instâncias dos componentes não selecionáveis "DEC" e "Jan" existem nos componentes de componentes não selecionáveis "Conjunto1" e "Conjunto2" e sob o subcomponente selecionável "Usage".

Se o componente "writerData" for explicitamente incluído em um backup ou restauração, todos os seus subcomponentes — mesmo aqueles no conjunto de componentes aninhados definido por "Usage" — serão [*incluídos implicitamente*](vssgloss-e.md)[*incluídos*](vssgloss-i.md) na operação.

Se o conjunto de componentes definido por "writerData" não for incluído explicitamente em um backup ou restauração, os componentes "Conjunto1", "Conjunto2" e "QueryLogs" (e suas instâncias de subcomponentes "DEC" e "Jan") não serão incluídos implicitamente na operação de backup ou restauração.

No entanto, mesmo se "writerData" não estiver incluído na operação, o "uso" do componente ainda será selecionável e ainda poderá ser incluído explicitamente em uma operação de backup ou restauração. Se for, os subcomponentes "Jan" e "DEC" serão incluídos implicitamente.

Outros pontos dignos de observação:

-   Os componentes selecionáveis "LicenseInfo" e "writerData" e os "executáveis" do componente não selecionável estão todos no mesmo nível na hierarquia de caminho lógico do *myWriter*: todos têm o mesmo caminho lógico **nulo** ou "", o caminho lógico raiz.
-   O "uso" do componente selecionável nunca deve ser incluído explicitamente em um backup, se seu pai selecionável ("writerData") for explicitamente incluído em uma operação de backup ou restauração.
-   Os componentes que definem conjuntos de componentes podem existir simplesmente por motivos organizacionais. Por exemplo, o componente "writerData" ou "uso", ou ambos, pode estar vazio; ou seja, nenhum [*conjunto de arquivos*](vssgloss-f.md) foi adicionado a eles usando o método [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . Os componentes ainda definem um conjunto de componentes.

 

 



