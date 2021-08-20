---
description: Os valores do Registro devem ser definidos para verbos lidarem com situações em que um usuário possa selecionar um único item, vários itens ou uma seleção de um item. Um verbo requer valores de Registro separados para cada uma dessas três situações às quais o verbo dá suporte.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Como empregar o modelo de seleção de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89028c7d2ce153582f45c140a0f32ca9f1714601c3e68bf36693b5955c904f71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049849"
---
# <a name="how-to-employ-the-verb-selection-model"></a>Como empregar o modelo de seleção de verbos

Os valores do Registro devem ser definidos para verbos lidarem com situações em que um usuário possa selecionar um único item, vários itens ou uma seleção de um item. Um verbo requer valores de Registro separados para cada uma dessas três situações às quais o verbo dá suporte.

## <a name="instructions"></a>Instruções


Especifique o valor MultiSelectModel para todos os verbos. Se o valor MultiSelectModel não for especificado, ele será inferido do tipo de implementação de verbo que você escolheu. Para métodos baseados em COM (como DropTarget e ExecuteCommand), o **Player** é assumido e, para os outros métodos, **Document** é assumido.

Os valores possíveis para o modelo de seleção de verbo são os seguinte:

1.  **Especifique** Único para verbos que suportam apenas uma única seleção.
2.  **Especifique** Player para verbos que suportam qualquer número de itens.
3.  **Especifique** Documento para verbos que criam uma janela de nível superior para cada item. Isso limita o número de itens que são ativados e ajuda a evitar a falta de recursos do sistema se o usuário abrir muitas janelas.

## <a name="remarks"></a>Comentários

Quando o número de itens selecionados não corresponder ao modelo de seleção de verbo ou for maior que os limites padrão descritos na tabela a seguir, o verbo não aparecerá.



| Tipo de implementação de verbo | Documento | Jogador    |
|-----------------------------|----------|-----------|
| Herdada                      | 15 itens | 100 itens |
| COM                         | 15 itens | Sem limite  |



 

A seguir estão exemplos de entradas do Registro que usam o valor MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



