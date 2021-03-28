---
description: A mistura de cores permite que um aplicativo crie novas cores combinando a cor da caneta ou do pincel com cores na imagem existente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Mistura de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091203"
---
# <a name="color-mixing"></a>Mistura de cores

A mistura de cores permite que um aplicativo crie novas cores combinando a cor da caneta ou do pincel com cores na imagem existente. O aplicativo pode escolher para desenhar a cor da caneta ou do pincel como está (desenhando efetivamente em qualquer imagem existente) ou para misturar a cor com as cores já presentes.

O modo mix de primeiro plano, às vezes chamado de operação de rasterização binária, determina como essas cores são misturadas. Um aplicativo pode mesclar cores, preservando todos os componentes de ambas as cores; mascarar cores, remover ou moderarr componentes que não são comuns; ou exclusivamente mascarar cores, remover ou moderarr componentes comuns. Há várias variações nessas operações básicas de mixagem.

A combinação de cores está sujeita à aproximação de cores. Se o resultado da mistura de cores for uma cor que o dispositivo não pode gerar, o sistema aproxima o resultado, usando uma cor que ele pode gerar. Se um aplicativo misturar cores diferentes, as cores individuais usadas para criar a cor diquerda serão misturadas e os resultados estarão sujeitos à aproximação de cor.

Um aplicativo define o modo de combinação de primeiro plano usando a função [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) e recupera o modo atual usando a função [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .

Embora haja um modo de combinação em segundo plano, esse modo não controla a mistura de cores. Em vez disso, especifica se uma cor de plano de fundo é usada ao desenhar linhas com estilo, pincéis hachurados e texto.

 

 



