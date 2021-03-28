---
description: Quando um aplicativo chama uma função de desenho para pintar uma forma, o sistema posiciona um pincel no início da operação de pintura e mapeia um pixel no bitmap do pincel para a área do cliente na origem da janela, que é o canto superior esquerdo da janela.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origem do pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560827"
---
# <a name="brush-origin"></a>Origem do pincel

Quando um aplicativo chama uma função de desenho para pintar uma forma, o sistema posiciona um pincel no início da operação de pintura e mapeia um pixel no bitmap do pincel para a área do cliente na *origem da janela*, que é o canto superior esquerdo da janela. As coordenadas do pixel que o sistema mapeia são chamadas de *origem do pincel*. A origem do pincel padrão está localizada no canto superior esquerdo do bitmap do pincel, nas coordenadas (0, 0). Em seguida, o sistema copia o pincel pela área do cliente, formando um padrão que é tão alto quanto o bitmap. A operação de cópia continua, linha por linha, até que toda a área do cliente seja preenchida. No entanto, o padrão de pincel é visível somente dentro dos limites da forma especificada.

Há instâncias em que a origem do pincel padrão não deve ser usada. Por exemplo, pode ser necessário que um aplicativo use o mesmo pincel para pintar os planos de fundo de suas janelas pai e filho e misturar o plano de fundo de uma janela filho com aquela da janela pai. Para fazer isso, o aplicativo deve redefinir a origem do pincel chamando a função [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) e deslocando a origem do número de pixels necessário. (Um aplicativo pode recuperar a origem do pincel atual chamando a função [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) .)

A ilustração a seguir mostra uma estrela de cinco pontas preenchida usando um pincel definido pelo aplicativo. A ilustração mostra uma imagem com zoom do pincel, bem como o local no qual ele foi mapeado no início da operação de pintura.

![ilustração mostrando que a origem do pincel está mapeada para a origem da janela](images/csbru-01.png)

 

 



