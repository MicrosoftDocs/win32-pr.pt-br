---
description: Durante a renderização, o pipeline interpola os dados de vértice em cada triângulo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolação de triângulo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a411f53351ccd5d3407b358b03e705677e9bf5a96a57b162016afe09332bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746256"
---
# <a name="triangle-interpolation-direct3d-9"></a>Interpolação de triângulo (Direct3D 9)

Durante a renderização, o pipeline interpola os dados de vértice em cada triângulo. Os dados de vértice podem ser uma ampla variedade de dados e podem incluir (mas não se limitam a): cor difusa, cor especular, alfa difuso (opacidade de triângulo), alfa especular e um fator de cinza (retirado do alfa especular para o pipeline de vértice de função fixa e do registro de cinza para pipeline de vértice programável). Os dados de vértice são definidos pela Declaração [de Vértice (Direct3D 9)](vertex-declaration.md).

Para alguns dados de vértice, a interpolação depende do modo de sombreamento atual, conforme mostrado na tabela a seguir.



| Modo de sombreamento | Descrição                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plano         | Somente o fator de nevoeiro é interpolado no modo de sombreamento simples. Para todos os outros valores interpolados, a cor do primeiro vértice no triângulo é aplicada em toda a face. |
| Gouraud      | A interpolação linear é executada entre todos os três vértices.                                                                                                               |



 

As cores difusas e realces especulares são tratados de forma diferente, dependendo do modelo de cor. No modelo de cor RGB, o sistema usa os componentes de cor vermelha, verde e azul na interpolação.

O componente alfa de uma cor é tratado como um valor interpolado separado porque drivers de dispositivo podem implementar transparência de duas maneiras diferentes: utilizando uma mesclagem de textura ou usando textura pontilhada.

Use o membro ShadeCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar quais formas de interpolação o driver de dispositivo atual dá suporte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistemas de coordenadas e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



