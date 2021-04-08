---
description: Sinalizadores de capacidade da coordenada de textura do driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920544"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Sinalizadores de capacidade da coordenada de textura do driver.



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definir                                 | Valor       | Descrição                                                                                                                                                                                                          |
| D3DTSS \_ TCI \_ PassThru                    | 0x00000000l | Use as coordenadas de textura especificadas contidas no formato de vértice. Esse valor é resolvido para zero.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Use o vértice normal, transformado no espaço da câmera, como as coordenadas de textura de entrada para a transformação textura desta etapa.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Use a posição do vértice, transformada no espaço da câmera, como as coordenadas de textura de entrada para a transformação textura desta etapa.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Use o vetor de reflexo, transformado no espaço da câmera, como a coordenada de textura de entrada para a transformação textura desta etapa. O vetor de reflexão é calculado a partir da posição do vértice de entrada e do vetor normal. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Use as coordenadas de textura especificadas para o mapeamento de esfera.                                                                                                                                                            |



 

Essas constantes são usadas por D3DTSS \_ TEXCOORDINDEX.

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



