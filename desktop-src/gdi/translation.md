---
description: Alguns aplicativos convertem (ou deslocam) objetos desenhados na área do cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Tradução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115af82d1e5b80fa4c50d081e6d042d2f2c9c8950f3b4b8f6ed09108df4c52bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613336"
---
# <a name="translation"></a>Tradução

Alguns aplicativos convertem (ou deslocam) objetos desenhados na área do cliente. chamando a [**função SetWorldTransform para**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) definir o espaço do mundo apropriado para a transformação de espaço na página. A função SetWorldTransform recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados. Os membros eDx e eDy do XFORM especificam os componentes de tradução horizontal e vertical, respectivamente.

Quando *ocorre* a conversão, cada ponto em um objeto é deslocado verticalmente, horizontalmente ou ambos por um valor especificado. A ilustração a seguir mostra um retângulo de 20 por 20 unidades que foi convertido para a direita por 10 unidades quando copiado do espaço de coordenadas do mundo para o espaço de coordenadas de página.

![ilustração mostrando um retângulo em uma posição no espaço do mundo e em uma posição diferente no espaço da página](images/cstrn-09.png)

Na ilustração anterior, a coordenada x de cada ponto no retângulo é 10 unidades maior que a coordenada x original.

A tradução horizontal pode ser representada pelo algoritmo a seguir.

``` syntax
x' = x + Dx 
```

Em que x' é a nova coordenada x, x é a coordenada x original e Dx é a distância horizontal movida.

A tradução vertical pode ser representada pelo algoritmo a seguir.

``` syntax
y' = y + Dy 
```

Em que y' é a nova coordenada y, y é a coordenada y original e Dy é a distância vertical movida.

As transformações de conversão horizontal e vertical podem ser combinadas em uma única operação usando uma matriz 3 por 3.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(As regras de multiplicação de matriz determinam que o número de linhas em uma matriz deve ser igual ao número de colunas na outra. O inteiro 1 na matriz x y 1 é um espaço reservado que foi adicionado \| para atender a esse \| requisito.)

A matriz 3 por 3 que produziu a transformação de tradução ilustrada contém os valores a seguir.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



