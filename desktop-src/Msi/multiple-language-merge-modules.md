---
description: Vários módulos de linguagem podem fornecer componentes com vários idiomas diferentes como um único arquivo composto.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Módulos de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f32d219e1071cd431117919d3eb3f3361d30213f59a26f9ec2cdf2e81e591b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943417"
---
# <a name="multiple-language-merge-modules"></a>Módulos de mesclagem de vários idiomas

Vários módulos de linguagem podem fornecer componentes com vários idiomas diferentes como um único arquivo composto. O design e a funcionalidade de vários módulos de mesclagem de idioma são semelhantes aos módulos de idioma único. Um módulo de mesclagem de vários idiomas tem mais de um idioma listado na Propriedade [**resumo do**](template-summary.md) modelo. O banco de dados de um módulo de mesclagem de vários idiomas contém todas as informações de instalação para vários idiomas. O MergeModule.CABde inet dentro de um módulo de mesclagem de vários idiomas contém todos os arquivos para todos os idiomas com suporte.

Ao aplicar um arquivo .msm de vários idiomas a um arquivo .msi, você deve indicar o idioma final do pacote de instalação após a mesclagem. No caso de um único módulo de mesclagem de idioma, a tabela Arquivo do módulo de mesclagem lista todos os arquivos presentes no gabinete MergeModule.CABinet. [](file-table.md) No caso de um módulo de mesclagem de vários idiomas, MergeModule.CABinet contém todos os arquivos para cada idioma com suporte do módulo, mas apenas o subconjunto de arquivos para o idioma final entra na tabela Arquivo do módulo. A ferramenta de mesclagem deve garantir que o módulo fornece o subconjunto de informações e arquivos necessários para o idioma final solicitado.

Cada módulo de mesclagem tem um idioma padrão especificado na coluna Idioma da tabela [ModuleSignature](modulesignature-table.md). O idioma padrão de um módulo de mesclagem também é mostrado como o primeiro idioma, ou apenas, na propriedade [**Resumo do**](template-summary.md) Modelo. Dependendo do idioma final solicitado e do idioma padrão do módulo, a ferramenta de mesclagem pode aplicar as transformação de idioma a um módulo de mesclagem de vários idiomas para que ele possa ser aberto no idioma solicitado ou uma aproximação do idioma solicitado. As transformaçãos de linguagem são inseridas dentro do módulo de mesclagem. As ferramentas de mesclagem devem aplicar as transformação de linguagem em conformidade com as seguintes regras gerais:

-   Se os idiomas padrão e final são os mesmos, o módulo pode ser mesclado sem usar as transformaçãos de idioma.
-   Se o idioma padrão for 0 (um módulo neutro de idioma), o módulo poderá ser mesclado sem usar as transformação de idioma.
-   Se o idioma final não for o idioma padrão, a ferramenta de mesclagem deverá aplicar uma das transformaçãos de idioma inseridas no módulo para alterar o módulo para o idioma final ou para uma aproximação do idioma final.

Por exemplo, nenhuma transformação de idioma será necessária se o idioma final for 1033 (inglês dos EUA) e o idioma padrão do módulo for 1033 (inglês dos EUA), 0 (idioma neutro) ou 9 (inglês genérico).

As transformação de idioma serão necessárias se o idioma final for 1033 (inglês dos EUA) e o idioma padrão for 1031 (alemão). Nesse caso, a ferramenta de mesclagem pode primeiro pesquisar no módulo de vários idiomas uma transformação de idioma inserida para 1033 (inglês dos EUA). Se isso falhar, ele poderá pesquisar uma transformação em um idioma com um LANGID primário correspondente, mesmo se o LANGID secundário não corresponder. Por exemplo, se a ferramenta não puder encontrar uma transformação para 1033 (inglês dos EUA), ela pesquisa uma transformação para 9 (inglês genérico). Se isso falhar, a ferramenta de mesclagem procurará uma transformação para 0 (idioma neutro). Se todas essas pesquisas de uma transformação adequada falharem, o módulo não será aberto.

Para obter mais informações, consulte [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).

 

 



