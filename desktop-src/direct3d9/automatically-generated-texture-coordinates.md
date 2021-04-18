---
title: Coordenadas de textura geradas automaticamente (Direct3D 9)
description: O sistema pode usar a posição de espaço da câmera transformada ou a normal de um vértice como coordenadas de textura, ou pode computar os três vetores de elemento usados para resolver um mapa de ambiente cúbico.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796234"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Coordenadas de textura geradas automaticamente (Direct3D 9)

O sistema pode usar a posição de espaço da câmera transformada ou a normal de um vértice como coordenadas de textura, ou pode computar os três vetores de elemento usados para resolver um mapa de ambiente cúbico. Como as coordenadas de textura que você especifica explicitamente em um vértice, você pode usar coordenadas de textura geradas automaticamente como entrada para transformações de coordenadas de textura.

As coordenadas de textura geradas automaticamente podem reduzir significativamente a largura de banda necessária para dados de geometria, eliminando a necessidade de coordenadas de textura explícitas no formato de vértice. Em muitos casos, as coordenadas de textura que o sistema gera podem ser usadas com transformações para produzir efeitos especiais. É claro que esse é um recurso de finalidade especial, e você usará coordenadas de textura explícitas para muitas ocasiões.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Configurando coordenadas de textura geradas automaticamente

Em C++, o estado de D3DTSS \_ TEXCOORDINDEX Texture-Stage (do tipo [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated) controla como o sistema gera coordenadas de textura.

Normalmente, esse estado instrui o sistema a usar um determinado conjunto de coordenadas de textura codificadas no formato de vértice. Quando você inclui os \_ sinalizadores D3DTSS TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION ou D3DTSS TCI CAMERASPACEREFLECTIONVECTOR \_ \_ no valor que você atribui a esse Estado, o comportamento do sistema é bastante diferente. Se qualquer um desses sinalizadores estiver presente, o estágio de textura ignorará as coordenadas de textura dentro do formato de vértice em favor das coordenadas que o sistema gera. Os significados para cada sinalizador são mostrados na lista a seguir.

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    Use o vértice normal, transformado para o espaço da câmera, como coordenadas de textura de entrada.

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    Use a posição do vértice, transformada no espaço da câmera, como coordenadas de textura de entrada.

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    Use o vetor de reflexo, transformado no espaço da câmera, como coordenadas de textura de entrada. O vetor de reflexão é calculado a partir da posição do vértice de entrada e do vetor normal.

Os sinalizadores de índice de coordenadas de textura são mutuamente exclusivos. Este exemplo usa:

-   A posição do vértice (em câmera-espaço) como as coordenadas de textura de entrada para este estágio de textura
-   O modo Wrap definido no estado de \_ RENDERIZAÇÃO D3DRENDERSTATE WRAP1


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Coordenadas de textura geradas automaticamente são mais úteis como valores de entrada para uma transformação de coordenadas de textura ou para eliminar a necessidade de seu aplicativo de computar vetores de três elementos para mapas de ambiente cúbico.

O mapeamento de esfera usa um mapa de textura de computação (no momento do modelo) que contém todo o ambiente, conforme refletido por uma esfera do Chrome. O Direct3D tem um recurso de geração de coordenadas de textura usando o estado de renderização D3DTSS \_ TCI \_ CAMERASPACENORMAL, que assume o normal do vértice no espaço da câmera e o coloca por meio de uma transformação de textura para gerar coordenadas de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processamento de coordenadas de textura](texture-coordinate-processing.md)
</dt> <dt>

[Transformações de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Mapeamento de ambiente cúbico (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
