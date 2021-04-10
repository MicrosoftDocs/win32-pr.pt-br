---
description: Quando um módulo é mesclado em um banco de dados que tem um idioma padrão diferente, a ferramenta de mesclagem pode precisar aplicar uma transformação de idioma ao módulo para fornecer o idioma final. Para obter mais informações, consulte vários módulos de mesclagem de idiomas.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Criando uma transformação de idioma para um módulo de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970c8908ddbf89e31f0fc7a415358bb887f0838e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169201"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Criando uma transformação de idioma para um módulo de mesclagem de vários idiomas

Quando um módulo é mesclado em um banco de dados que tem um idioma padrão diferente, a ferramenta de mesclagem pode precisar aplicar uma transformação de idioma ao módulo para fornecer o idioma final. Para obter mais informações, consulte [vários módulos de mesclagem de idiomas](multiple-language-merge-modules.md).

As transformações de idioma são armazenadas no arquivo. msm do módulo e devem ter o nome e o formato: MergeModule. lang \# \# \# \# . O \# \# \# \# representa o [LangID](localizing-the-error-and-actiontext-tables.md) de até quatro dígitos do idioma final. Por exemplo, MergeModule. Lang1033, MergeModule. Lang9 e MergeModule. Lang0 para transformações para o inglês americano, o mundo inglês e o idioma neutro. Elas são as mesmas [transformações incorporadas](embedded-transforms.md) e você pode adicioná-las a subarmazenamentos no arquivo. msm.

A transformação de idioma deve fazer o seguinte:

-   Altere o idioma padrão na coluna idioma da [tabela ModuleSignature](modulesignature-table.md) para o novo idioma do módulo.
-   Altere o idioma padrão na coluna idioma da [tabela ModuleComponents](modulecomponents-table.md) para o novo idioma do módulo. A transformação pode adicionar ou remover linhas desta tabela.
-   Se necessário, altere o idioma na coluna RequiredLanguage ou adicione ou exclua linhas para a [tabela ModuleDependency](moduledependency-table.md).
-   Se necessário, altere o idioma na coluna ExcludedLanguage ou adicione ou exclua linhas para a [tabela ModuleExclusion](moduleexclusion-table.md).
-   A transformação pode executar qualquer operação de transformação válida no módulo, incluindo adicionar ou remover componentes, arquivos, entradas de registro ou ações.

Observe que a aplicação de uma transformação de idioma ao abrir o módulo não altera o idioma padrão ou os idiomas com suporte no módulo, ele apenas altera o idioma que está sendo solicitado. Portanto, a propriedade de [**Resumo do modelo**](template-summary.md) não é alterada, ela já deve listar todos os idiomas com suporte do módulo com o idioma padrão listado primeiro.

Todos os arquivos necessários para todas as transformações de linguagem possíveis normalmente são armazenados em um único arquivo de gabinete incluído com o módulo. Como não é prático fazer com que a transformação de linguagem modifique esse arquivo de gabinete, é melhor usar uma sequência de arquivos global no arquivo de gabinete, na [tabela de arquivos](file-table.md)e na transformação de idioma. Para obter detalhes, consulte [ordenando a sequência de arquivos no cab de um módulo de mesclagem de vários idiomas](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



