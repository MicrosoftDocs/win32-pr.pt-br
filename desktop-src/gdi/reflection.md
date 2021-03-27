---
description: Alguns aplicativos fornecem recursos que refletem (ou espelham) objetos desenhados na área do cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967601"
---
# <a name="reflection"></a>Reflexão

Alguns aplicativos fornecem recursos que refletem (ou espelham) objetos desenhados na área do cliente. Os aplicativos que contêm recursos de reflexão usam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir os valores apropriados no espaço mundial para a transformação de espaço em página. Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados. Os membros eM11 e eM22 do XFORM especificam os componentes de reflexo horizontal e vertical, respectivamente.

A *transformação reflexão* cria uma imagem espelho de um objeto em relação ao eixo x ou y. Em suma, a reflexão é apenas uma escala negativa. Para produzir uma reflexão horizontal, as coordenadas x são multiplicadas por 1. Para produzir uma reflexão vertical, as coordenadas y são multiplicadas por 1.

A reflexão horizontal pode ser representada pelo seguinte algoritmo:

``` syntax
x' = -x 
```

em que x é a coordenada x e x ' é o resultado da reflexão.

A matriz 2-por-2 que produziu a reflexão horizontal contém os seguintes valores:

``` syntax
|-1    0| 
|0     1| 
```

A reflexão vertical pode ser representada pelo seguinte algoritmo:

``` syntax
y' = -y 
```

em que y é a coordenada y e y ' é o resultado da reflexão.

A matriz 2-por-2 que produziu a reflexão vertical contém os seguintes valores:

``` syntax
|1    0| 
|0   -1| 
```

As operações de reflexão horizontal e de reflexo vertical podem ser combinadas em uma única operação usando a seguinte matriz 2-por-2:

``` syntax
|-1    0| 
|0    -1| 
```

 

 



