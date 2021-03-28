---
description: Os valores do registro devem ser definidos para verbos para lidar com situações em que um usuário pode selecionar um único item, vários itens ou uma seleção de um item. Um verbo requer valores de registro separados para cada uma dessas três situações às quais o verbo dá suporte.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Como empregar o modelo de seleção de verbo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967906"
---
# <a name="how-to-employ-the-verb-selection-model"></a>Como empregar o modelo de seleção de verbo

Os valores do registro devem ser definidos para verbos para lidar com situações em que um usuário pode selecionar um único item, vários itens ou uma seleção de um item. Um verbo requer valores de registro separados para cada uma dessas três situações às quais o verbo dá suporte.

## <a name="instructions"></a>Instruções


Especifique o valor de MultiSelectModel para todos os verbos. Se o valor de MultiSelectModel não for especificado, ele será inferido do tipo de implementação de verbo que você escolheu. Para métodos baseados em COM (como DropTarget e ExecuteCommand), o **Player** é assumido e, para os outros métodos, o **documento** é assumido.

Os valores possíveis para o modelo de seleção de verbo são os seguintes:

1.  Especifique **single** para verbos que dão suporte a apenas uma única seleção.
2.  Especifique o **Player** para verbos que dão suporte a qualquer número de itens.
3.  Especifique o **documento** para verbos que criam uma janela de nível superior para cada item. Isso limita o número de itens que são ativados e ajuda a evitar a execução de recursos do sistema se o usuário abrir muitas janelas.

## <a name="remarks"></a>Comentários

Quando o número de itens selecionados não corresponde ao modelo de seleção de verbo ou é maior que os limites padrão descritos na tabela a seguir, o verbo não aparece.



| Tipo de implementação de verbo | Documento | Jogador    |
|-----------------------------|----------|-----------|
| Herdada                      | 15 itens | 100 itens |
| COM                         | 15 itens | Sem limite  |



 

Veja a seguir as entradas de registro de exemplo que usam o valor MultiSelectModel.

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

 

 



