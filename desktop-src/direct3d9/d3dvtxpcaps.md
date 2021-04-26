---
description: Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7e5d423169e561df28b5d69017c77a71e183
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998653"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.



| \#definir                                | Descrição                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | O dispositivo pode realizar luzes direcionais.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | O dispositivo pode fazer o visualizador local.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Quando esse limite é definido, o dispositivo dá suporte aos Estados de material de cor: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DiffuseMaterialSource, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS \_ SPECULARMATERIALSOURCE. |
| D3DVTXPCAPS \_ \_ TEXGEN \_ NONLOCALVIEWER | O dispositivo não oferece suporte à geração de textura no modo de visualizador não local.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | O dispositivo pode fazer luzes posicionais (inclui ponto e spot).                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | O dispositivo pode fazer texgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | O dispositivo dá suporte a D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| \_Interpolação D3DVTXPCAPS                   | O dispositivo pode fazer a interpolação de vértice.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



