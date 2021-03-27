---
description: Alguns aplicativos traduzem (ou deslocam) objetos desenhados na área do cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Tradução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988289"
---
# <a name="translation"></a>Tradução

Alguns aplicativos traduzem (ou deslocam) objetos desenhados na área do cliente. chamando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir o espaço mundial apropriado para a transformação de espaço em página. A função SetWorldTransform recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados. Os membros eDx e eDy do XFORM especificam os componentes de tradução horizontal e vertical, respectivamente.

Quando ocorre a *conversão* , cada ponto em um objeto é deslocado verticalmente, horizontalmente ou ambos, por um valor especificado. A ilustração a seguir mostra um retângulo de 20 por 20 unidades que foi traduzido para a direita por 10 unidade quando copiado do espaço de coordenadas mundiais para o espaço de coordenadas de página.

![ilustração mostrando um retângulo em uma posição no espaço do mundo e em uma posição diferente no espaço da página](images/cstrn-09.png)

Na ilustração anterior, a coordenada x de cada ponto no retângulo é de 10 unidades acima da coordenada x original.

A tradução horizontal pode ser representada pelo seguinte algoritmo.

``` syntax
x' = x + Dx 
```

Em que x ' é a nova coordenada x, x é a coordenada x original e DX é a distância horizontal movida.

A tradução vertical pode ser representada pelo algoritmo a seguir.

``` syntax
y' = y + Dy 
```

Onde y ' é a nova coordenada y, y é a coordenada y original e dy é a distância vertical movida.

As transformações de translação horizontal e vertical podem ser combinadas em uma única operação usando uma matriz 3-by-3.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(As regras de estado de multiplicação de matriz que o número de linhas em uma matriz devem ser iguais ao número de colunas no outro. O inteiro 1 na matriz \| x y 1 \| é um espaço reservado que foi adicionado para atender a esse requisito.)

A matriz 3-by-3 que produziu a transformação de tradução ilustrada contém os valores a seguir.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



