---
description: Os parâmetros de neblina são controlados por meio de Estados de processamento de dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parâmetros de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825708"
---
# <a name="fog-parameters-direct3d-9"></a>Parâmetros de neblina (Direct3D 9)

Os parâmetros de neblina são controlados por meio de Estados de processamento de dispositivo. Os tipos de neblina de pixel e Vertex dão suporte a todas as fórmulas de neblina introduzidas em [fórmulas de neblina (Direct3D 9)](fog-formulas.md). O tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) define constantes que você pode usar para identificar a fórmula de neblina que você deseja que o Microsoft Direct3D use. O \_ estado de RENDERIZAÇÃO D3DRS FOGTABLEMODE controla o modo de neblina usado pelo Direct3D para a neblina de pixels e o \_ estado de renderização D3DRS FOGVERTEXMODE controla o modo de neblina de vértice.

Ao usar a fórmula de neblina linear, você define as distâncias inicial e final por meio dos \_ Estados de RENDERIZAÇÃO D3DRS FOGSTART e D3DRS \_ FOGEND. A maneira como o sistema interpreta esses valores depende do tipo de neblina que seu aplicativo usa – pixel ou neblina de vértice-e, ao usar a neblina de pixel, se a profundidade baseada em z ou w estiver sendo usada. A tabela a seguir resume os tipos de neblina e suas unidades de início e de término.



| Tipo de neblina  | Unidades de início/término da neblina      |
|-----------|--------------------------|
| Pixel (Z) | Espaço \[ de dispositivo 0,0, 1,0\] |
| Pixel (W) | Espaço da câmera             |
| Vértice    | Espaço da câmera             |



 

O \_ estado de RENDERIZAÇÃO D3DRS FOGDENSITY controla a densidade de neblina aplicada quando uma fórmula de neblina exponencial é habilitada. A densidade de neblina é essencialmente um fator de ponderação, variando de 0,0 a 1,0 (inclusivo), que dimensiona o valor de distância no expoente.

A cor que o sistema usa para mesclagem de neblina é controlada por meio do \_ estado de processamento do dispositivo D3DRS FOGCOLOR. Para obter mais informações, consulte [cor de neblina (Direct3D 9)](fog-color.md) e [mistura de neblina (Direct3D 9)](fog-blending.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de neblina](fog-types.md)
</dt> </dl>

 

 
