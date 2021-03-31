---
description: O idioma padrão para um módulo de mesclagem é o idioma listado na tabela ModuleSignature do módulo antes que as transformações de idioma sejam aplicadas. Esse também é o primeiro idioma listado na propriedade de resumo do modelo.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Escolhendo o idioma padrão de um módulo de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828038"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Escolhendo o idioma padrão de um módulo de mesclagem de vários idiomas

O idioma padrão para um módulo de mesclagem é o idioma listado na [tabela ModuleSignature](modulesignature-table.md) do módulo antes que as transformações de idioma sejam aplicadas. Esse também é o primeiro idioma listado na propriedade de [**Resumo do modelo**](template-summary.md) .

O idioma padrão do módulo deve ser uma das linguagens mais específicas às quais você dá suporte, pois o idioma padrão sempre é verificado primeiro e, se ele satisfizer o idioma solicitado, ele será usado mesmo se outra linguagem for uma correspondência melhor. Por exemplo, se um módulo der suporte a 1033 e a 0, 1033 deverá ser o idioma padrão. Se 0 fosse o idioma padrão, ele sempre atenderia a qualquer solicitação, e a transformação 1033 nunca seria usada, mesmo se 1033 for o idioma exato solicitado.

 

 



