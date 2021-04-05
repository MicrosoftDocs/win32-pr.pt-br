---
description: ICEM14 valida a coluna Value da tabela ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091020"
---
# <a name="icem14"></a>ICEM14

ICEM14 valida a coluna Value da [tabela ModuleSubstitution](modulesubstitution-table.md).

## <a name="result"></a>Resultado

ICEM14 posta os erros a seguir.



| Erro                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A cadeia de caracteres de substituição na coluna ModuleSubstitution. Value na linha \[ 1 \] . \[ 2 \] . \[ 3 \] não foi encontrado na Tabela ModuleConfiguration.                                 | \[1 \] . \[ 2 \] . \[ 3 \] refere-se a uma chave primária *Table. Row. Column* para uma linha na tabela ModuleSubstitution. O modelo de formatação no campo valor dessa linha não corresponde a uma linha de atributos configuráveis na [Tabela ModuleConfiguration](moduleconfiguration-table.md).                                                            |
| Na tabela ModuleSubstitution na linha \[ 1 \] . \[ 2 \] . \[ 3 \] , um item configurável é indicado na tabela '% s'. A tabela '% s' não deve conter itens configuráveis. | Uma das tabelas a seguir está listada na coluna tabela da tabela ModuleSubstitution: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)ou [ModuleSignature](modulesignature-table.md). Essas tabelas não podem conter campos configuráveis. |
| Na tabela ModuleSubstitution na linha \[ 1 \] . \[ 2 \] . \[ 3 \] , uma cadeia de caracteres de substituição vazia foi especificada.                                                               | O modelo de formatação no campo valor dessa linha não corresponde a uma linha de atributos configuráveis na [Tabela ModuleConfiguration](moduleconfiguration-table.md).                                                                                                                                                                    |



 

ICEM14 posta o aviso a seguir.



| Aviso                                                                  | Significado                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| A tabela ModuleSubstitution existe, mas a Tabela ModuleConfiguration está ausente | A Tabela ModuleConfiguration está ausente. |



 

## <a name="table-used-during-execution"></a>Tabela usada durante a execução

[Tabela ModuleSubstitution](modulesubstitution-table.md)

[Tabela ModuleConfiguration](moduleconfiguration-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



