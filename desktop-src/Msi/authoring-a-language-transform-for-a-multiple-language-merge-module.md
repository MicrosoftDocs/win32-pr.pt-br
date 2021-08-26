---
description: Quando um módulo é mesclado em um banco de dados que tem um idioma padrão diferente, a ferramenta de mesclagem pode precisar aplicar uma transformação de idioma ao módulo para fornecer o idioma final. Para obter mais informações, consulte Multiple Language Merge Modules.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Como fazer uma transformação de linguagem para um módulo de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9a9c2294d310959bcd82f13010c88eb513e40ad4536c4dbca61e50d260873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078056"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Como fazer uma transformação de linguagem para um módulo de mesclagem de vários idiomas

Quando um módulo é mesclado em um banco de dados que tem um idioma padrão diferente, a ferramenta de mesclagem pode precisar aplicar uma transformação de idioma ao módulo para fornecer o idioma final. Para obter mais informações, consulte [Multiple Language Merge Modules](multiple-language-merge-modules.md).

As transformaçãos de idioma são armazenadas no arquivo .msm do módulo e devem ter o nome e o formato: MergeModule.Lang. \# \# \# \# O \# \# \# \# representa o [LANGID](localizing-the-error-and-actiontext-tables.md) de até quatro dígitos do idioma final. Por exemplo, MergeModule.Lang1033, MergeModule.Lang9 e MergeModule.Lang0 para transformar em inglês dos EUA, inglês mundial e neutralidade de idioma. Elas são as mesmas que As [Transformaçãos Inseridas](embedded-transforms.md) e você pode adicioná-las a substorages no arquivo .msm.

A transformação de linguagem deve fazer o seguinte:

-   Altere o idioma padrão na coluna Idioma da tabela [ModuleSignature](modulesignature-table.md) para o novo idioma do módulo.
-   Altere o idioma padrão na coluna Idioma da [tabela ModuleComponents](modulecomponents-table.md) para o novo idioma do módulo. A transformação pode adicionar ou remover linhas dessa tabela.
-   Se necessário, altere o idioma na coluna RequiredLanguage ou adicione ou exclua linhas para a [tabela ModuleDependency](moduledependency-table.md).
-   Se necessário, altere o idioma na coluna ExcludedLanguage ou adicione ou exclua linhas à [tabela ModuleExclusion](moduleexclusion-table.md).
-   A transformação pode executar qualquer operação de transformação válida no módulo, incluindo a adição ou remoção de componentes, arquivos, entradas do Registro ou ações.

Observe que a aplicação de uma transformação de idioma ao abrir o módulo não altera o idioma padrão ou os idiomas com suporte do módulo, apenas altera o idioma que está sendo solicitado. Portanto, a propriedade [**Resumo**](template-summary.md) do Modelo não muda, ela já deve listar todos os idiomas com suporte pelo módulo com o idioma padrão listado primeiro.

Todos os arquivos necessários para todas as possíveis transformaçãos de idioma são normalmente armazenados em um único arquivo de gabinete incluído no módulo. Como não é prático fazer com que a transformação de linguagem modifique esse arquivo de gabinete, é melhor usar uma sequência de arquivos global no arquivo de [gabinete,](file-table.md)tabela de arquivos e transformação de idioma. Para obter detalhes, consulte [Ordenando a sequência de arquivos no CAB de um módulo de mesclagem de vários idiomas](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



