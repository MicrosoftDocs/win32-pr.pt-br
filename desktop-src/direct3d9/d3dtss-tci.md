---
description: Sinalizadores de funcionalidade da coordenada de textura do driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58746f17eb18b679a4dfe4957ac46236baeec35d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342971"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Sinalizadores de funcionalidade da coordenada de textura do driver.



| \#Definir                                 | Valor       | Descrição                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x0000000L | Use as coordenadas de textura especificadas contidas no formato de vértice. Esse valor é resolvido como zero.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Use o vértice normal, transformado no espaço da câmera, como as coordenadas de textura de entrada para a transformação de textura deste estágio.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Use a posição do vértice, transformada no espaço da câmera, como as coordenadas de textura de entrada para a transformação de textura deste estágio.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Use o vetor de reflexão, transformado no espaço da câmera, como a coordenada de textura de entrada para a transformação de textura deste estágio. O vetor de reflexão é calculado da posição do vértice de entrada e do vetor normal. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Use as coordenadas de textura especificadas para o mapeamento de esfera.                                                                                                                                                            |



 

Essas constantes são usadas por D3DTSS \_ TEXCOORDINDEX.

## <a name="constant-information"></a>Informações constantes



|  Requisito                        | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



