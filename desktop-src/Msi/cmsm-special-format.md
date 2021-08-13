---
description: Determinados valores usados com módulos de mesclagem configuráveis exigem manipulação de texto especial.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: CMSM formato especial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8521c422d62980da0d222f8a8fc8395afa40b68bfd65c5600298372b1035f97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252136"
---
# <a name="cmsm-special-format"></a>CMSM formato especial

Determinados valores usados com módulos de mesclagem configuráveis exigem manipulação de texto especial. Uma cadeia de texto descrita como estando no "formato especial CMSM" trata o ponto e vírgula (;) e caracteres iguais (=) como caracteres reservados usados pela ferramenta de mesclagem do cliente ou Mergemod.dll.

O formato especial CMSM é usado atualmente nos seguintes locais:

-   A coluna de linha da [tabela ModuleSubstitution](modulesubstitution-table.md).
-   A coluna Value da [tabela ModuleSubstitution](modulesubstitution-table.md).
-   A coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md) quando o campo de bits é o valor na coluna de formato.
-   A coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md) quando Text é o valor na coluna Format e enum é o valor na coluna Type.
-   A coluna DefaultValue da [Tabela ModuleConfiguration](moduleconfiguration-table.md) quando Key é o valor na coluna Format.
-   Itens configuráveis no formato de chave usado pelo [**método ProvideTextData**](configuremodule-providetextdata.md).

Para inserir ponto e vírgulas literais ou caracteres iguais em um valor no formato especial CMSM, Prefixe o caractere com um caractere de barra invertida (' \\ '). Uma barra invertida literal pode ser representada por duas barras invertidas. Um único caractere prefixado por uma única barra invertida é convertido em um único caractere, mesmo que o escape do caractere não seja necessário.

Se um ponto-e-vírgula ou caractere de igual não for prefixado por uma barra invertida, mas não tiver um comportamento definido no contexto do valor, a cadeia de caracteres resultante será indefinida. Por exemplo, a coluna DefaultValue da Tabela ModuleConfiguration está no formato especial CMSM para todos os itens de chave porque o caractere ponto-e-vírgula é o delimitador de coluna. Embora o caractere igual não tenha significado especial nessa cadeia de caracteres, os caracteres literais iguais ainda devem ser ignorados nessa cadeia de caracteres.

 

 



