---
description: Vários módulos de linguagem podem fornecer componentes com várias linguagens diferentes como um único arquivo composto.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Vários módulos de mesclagem de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f32d219e1071cd431117919d3eb3f3361d30213f59a26f9ec2cdf2e81e591b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943417"
---
# <a name="multiple-language-merge-modules"></a>Vários módulos de mesclagem de idioma

Vários módulos de linguagem podem fornecer componentes com várias linguagens diferentes como um único arquivo composto. O design e a funcionalidade de módulos de mesclagem de vários idiomas são semelhantes aos módulos de linguagem única. Um módulo de mesclagem de vários idiomas tem mais de um idioma listado na propriedade de [**Resumo do modelo**](template-summary.md) . O banco de dados de um módulo de mesclagem de vários idiomas contém todas as informações de configuração de vários idiomas. O MergeModule.CABgabinete inet dentro de um módulo de mesclagem de vários idiomas contém todos os arquivos para todos os idiomas com suporte.

Ao aplicar um arquivo. msm com vários idiomas a um arquivo .msi, você deve indicar o idioma final do pacote de instalação após a mesclagem. No caso de um único módulo de mesclagem de idioma, a [tabela de arquivos](file-table.md) do módulo de mesclagem lista todos os arquivos presentes no MergeModule.CABgabinete inet. No caso de um módulo de mesclagem de vários idiomas, MergeModule.CABo inet contém todos os arquivos para cada idioma com suporte no módulo, mas apenas o subconjunto de arquivos para o idioma final entra na tabela de arquivos do módulo. A ferramenta de mesclagem deve garantir que o módulo forneça o subconjunto de informações e arquivos necessários para a linguagem final solicitada.

Cada módulo de mesclagem tem um idioma padrão especificado na coluna idioma da [tabela ModuleSignature](modulesignature-table.md). O idioma padrão de um módulo de mesclagem também é mostrado como o primeiro, ou apenas, o idioma na propriedade de [**Resumo do modelo**](template-summary.md) . Dependendo da linguagem final solicitada e do idioma padrão do módulo, a ferramenta de mesclagem pode aplicar transformações de idioma a um módulo de mesclagem de vários idiomas para que ele possa ser aberto no idioma solicitado ou uma aproximação do idioma solicitado. As transformações de idioma são inseridas dentro do módulo de mesclagem. As ferramentas de mesclagem devem aplicar transformações de linguagem em conformidade com as seguintes regras gerais:

-   Se os idiomas padrão e final forem os mesmos, o módulo poderá ser mesclado sem usar transformações de linguagem.
-   Se o idioma padrão for 0 (um módulo de linguagem neutra), o módulo poderá ser mesclado sem usar transformações de linguagem.
-   Se o idioma final não for o idioma padrão, a ferramenta de mesclagem deverá aplicar uma das transformações de idioma inseridas no módulo para alterar o módulo para o idioma final ou para uma aproximação da linguagem final.

Por exemplo, nenhuma transformação de linguagem será necessária se o idioma final for 1033 (inglês americano) e o idioma padrão do módulo for 1033 (inglês americano), 0 (neutro de idioma) ou 9 (Inglês genérico).

As transformações de idioma são necessárias se o idioma final for 1033 (inglês americano) e o idioma padrão for 1031 (alemão). Nesse caso, a ferramenta de mesclagem pode primeiro Pesquisar o módulo vários idiomas para uma transformação de linguagem incorporada para 1033 (inglês americano). Se isso falhar, ele poderá pesquisar uma transformação em um idioma com um LANGid primário correspondente, mesmo se o LANGid secundário não corresponder. Por exemplo, se a ferramenta não conseguir encontrar uma transformação para 1033 (inglês americano), ela pesquisará uma transformação de 9 (Inglês genérico). Se isso falhar, a ferramenta de mesclagem pesquisará uma transformação em 0 (neutro à linguagem). Se todas essas pesquisas de uma transformação adequada falharem, o módulo não será aberto.

Para obter mais informações, consulte [criando módulos de mesclagem de vários idiomas](authoring-multiple-language-merge-modules.md).

 

 



