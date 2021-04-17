---
description: Crítico para organizar de quais arquivos de qual gravador deve ser feito backup ou restaurado é o conceito de um componente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Componentes de metadados do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811380"
---
# <a name="vss-metadata-components"></a>Componentes de metadados do VSS

Crítico para organizar de quais arquivos de qual gravador deve ser feito backup ou restaurado é o conceito de um [*componente*](vssgloss-c.md).

Os componentes permitem que um gravador indique para um mecanismo de backup como seus arquivos devem ser organizados, as dependências entre os arquivos e os tipos de dados que esses arquivos podem conter. Isso permite que um mecanismo de backup decida como armazenar arquivos para obter máxima eficiência.

Além disso, os aplicativos baseados em VSS usam componentes como os blocos de construção para seus metadados e a mídia para a comunicação do gravador/solicitante.

Gravadores e solicitantes armazenam informações sobre componentes separadamente — no documento de metadados do gravador e no documento de componentes de backup, respectivamente, e as informações diferem em cada representação.

As informações de componente nos documentos de metadados do gravador incluem o seguinte:

-   Informações de apenas um gravador em cada documento
-   Todos os componentes do escritor, se eles podem ser [*explicitamente incluídos*](vssgloss-e.md) ou devem ser [*incluídos implicitamente*](vssgloss-i.md) em uma operação de backup ou restauração
-   Informações de [*caminho lógico*](vssgloss-l.md) usadas para associar uma selecionável para o componente de backup com um determinado não selecionável para componentes de backup, formando assim um conjunto de componentes
-   As informações do [*conjunto de arquivos*](vssgloss-f.md) — caminho, especificação de arquivo e sinalizador de recursão — gerenciado para cada componente

Os documentos de metadados do gravador também contêm informações de metadados no nível do gravador, como métodos de restauração e mapeamentos de local alternativos para restauração. Os documentos de metadados do gravador são somente leitura. A interface para examinar essas informações é [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).

As informações de componente em documentos de componentes de backup incluem o seguinte:

-   Apenas informações sobre componentes explicitamente incluídos
-   Informações de metadados em nível de gravador, como mapeamentos e restaurações de local alternativos
-   Informações de estado que descrevem uma operação de backup ou restauração

Os documentos de componente de backup não contêm informações sobre [*conjuntos de arquivos*](vssgloss-f.md)de componentes. Os documentos do componente de backup não são somente leitura e podem ser modificados pelo gravador. A interface para acessar essas informações é [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

O ciclo de vida e a relação entre as duas expressões de um componente podem ser compreendidos da seguinte maneira:

-   Os gravadores são responsáveis pelas definições iniciais dos componentes.
-   Um solicitante examina os metadados de todos os gravadores e seus componentes.
-   Das informações de seleção e caminho lógico dos componentes, um solicitante determina quais componentes devem ser incluídos explicitamente, que podem ser incluídos explicitamente, que definem os conjuntos de componentes e que são membros de conjuntos de componentes.
-   Um solicitante adiciona os componentes que exigem inclusão explícita e inclui implicitamente subcomponentes em [*conjuntos de componentes*](/windows) (cujas informações não estão no documento de componentes de backup).
-   Ao manipular eventos, gravadores e solicitantes podem modificar e examinar as informações de componente armazenadas no documento de componentes de backup para coordenar suas atividades.

As informações de componente do gravador e do solicitante são necessárias para executar corretamente as operações de backup e restauração, e ambas devem ser armazenadas com os dados submetidos a backup:

-   [Tipos de componentes](component-types.md)
-   [Definição de componentes por gravadores](definition-of-components-by-writers.md)
-   [Uso de componentes pelo solicitante](use-of-components-by-the-requestor.md)

 

 
