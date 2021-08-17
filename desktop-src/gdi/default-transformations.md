---
description: Sempre que um aplicativo cria um DC e imediatamente começa a chamar funções de desenho ou saída do GDI, ele aproveita o espaço de página padrão para o espaço do dispositivo e o espaço do dispositivo para as transformações da área do cliente.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Transformações padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba34effd9d6d43ab3b0abc740250c58788a8ce2f1556e89c92b78af823e58c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469676"
---
# <a name="default-transformations"></a>Transformações padrão

Sempre que um aplicativo cria um DC e imediatamente começa a chamar funções de desenho ou saída do GDI, ele aproveita o espaço de página padrão para o espaço do dispositivo e o espaço do dispositivo para as transformações da área do cliente. Uma transformação de espaço de mundo para página não pode acontecer até que o aplicativo chame primeiro a função [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) para definir o modo como GM \_ Advanced e, em seguida, chama a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .

O uso de \_ texto mm (o espaço de página padrão para transformação de dispositivo-espaço) resulta em um mapeamento de um para um; ou seja, um determinado ponto no espaço de página é mapeado para o mesmo ponto no espaço do dispositivo. Como mencionado anteriormente, essa transformação não é especificada por uma matriz. Em vez disso, é obtido dividindo a largura do visor pela largura da janela e a altura do visor pela altura da janela. No caso padrão, as dimensões do visor são de 1 pixel por 1 pixel e as dimensões da janela são de 1 a unidade de página em 1-unidade de página.

A transformação dispositivo-espaço para dispositivo físico (área de cliente, área de trabalho ou papel de impressora) sempre resulta em um mapeamento de um para um; ou seja, uma unidade no espaço do dispositivo é sempre equivalente a uma unidade na área do cliente, na área de trabalho ou em uma página. A única finalidade dessa transformação é a tradução; Ele garante que a saída apareça corretamente na janela de um aplicativo, independentemente de onde essa janela seja movida na área de trabalho.

O aspecto único do texto MM \_ é a orientação do eixo y no espaço da página. Em \_ texto mm, o eixo y positivo se estende para baixo e o eixo y negativo se estende para cima.

 

 



