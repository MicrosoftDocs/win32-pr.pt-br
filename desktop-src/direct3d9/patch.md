---
description: Define um B&\# 233; patch de controle zier. A matriz define os pontos de controle para o patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825491"
---
# <a name="patch"></a>Patch

Define um patch de controle de Bézier. A matriz define os pontos de controle para o patch.

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

Em que:

-   nControlIndices-número de índices de ponto de controle.
-   array DWORD controlIndices \[ nControlIndices \] -matriz de índices de ponto de controle.

O tipo de patch é definido pelo número de pontos de controle, conforme mostrado na tabela a seguir.



| Número de pontos de controle | Tipo                              |
|--------------------------|-----------------------------------|
| 10                       | Patch triangular Bézier cúbico     |
| 15                       | Patch triangular de Bézier quarto   |
| 16                       | Patch de retângulo quádruplo de Bézier cúbica |



 

A ordem dos pontos de controle é fornecida em um padrão de espiral, conforme mostrado nos diagramas a seguir para patches triangulares e retangulares.

Os patches triangulares usam o padrão a seguir.

![diagrama do padrão para patches triangulares](images/tripatch.png)

Os patches retangulares usam o padrão a seguir.

![diagrama do padrão para patches retangulares](images/quadpatch.png)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



