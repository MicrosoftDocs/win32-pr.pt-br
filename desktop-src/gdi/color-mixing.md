---
description: A combinação de cores permite que um aplicativo crie novas cores combinando a caneta ou a cor do pincel com cores na imagem existente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Combinação de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1adde68360d7050e0cebb6e7d5ac073b36a3c18c3687990c1f2aea6a5719f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105725"
---
# <a name="color-mixing"></a>Combinação de cores

A combinação de cores permite que um aplicativo crie novas cores combinando a caneta ou a cor do pincel com cores na imagem existente. O aplicativo pode optar por desenhar a caneta ou a cor do pincel como está (desenhando efetivamente em qualquer imagem existente) ou para combinar a cor com as cores já presentes.

O modo de combinação de primeiro plano, às vezes chamado de operação de raster binário, determina como essas cores são misturadas. Um aplicativo pode mesclar cores, preservando todos os componentes de ambas as cores; mascarar cores, remover ou moderar componentes que não são comuns; ou mascarar exclusivamente as cores, removendo ou moderando componentes que são comuns. Há várias variações nessas operações de combinação básicas.

A combinação de cores está sujeita à aproximação de cores. Se o resultado da combinação de cores for uma cor que o dispositivo não pode gerar, o sistema aproximará o resultado, usando uma cor que ele pode gerar. Se um aplicativo misturar cores dithered, as cores individuais usadas para criar a cor dithered serão misturadas e os resultados serão sujeitos à aproximação de cores.

Um aplicativo define o modo de combinação de primeiro plano usando a função [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) e recupera o modo atual usando a [**função GetROP2.**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)

Embora haja um modo de combinação de plano de fundo, esse modo não controla a combinação de cores. Em vez disso, especifica se uma cor da tela de fundo é usada ao desenhar linhas com estilo, pincéis e texto.

 

 



