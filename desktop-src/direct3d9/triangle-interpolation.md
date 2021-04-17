---
description: Durante a renderização, o pipeline interpola os dados de vértice em cada triângulo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolação de triângulo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791464"
---
# <a name="triangle-interpolation-direct3d-9"></a>Interpolação de triângulo (Direct3D 9)

Durante a renderização, o pipeline interpola os dados de vértice em cada triângulo. Os dados de vértice podem ser uma grande variedade de dados e podem incluir (mas não se limitam a): cor difusa, cor especular, alfa difusa (opacidade de triângulo), alfanuméricos de especulação e um fator de neblina (tirado da especulação alfa para pipeline de vértice de função fixa e do registro de neblina para pipeline de vértice programável). Os dados de vértice são definidos pela [declaração de vértice (Direct3D 9)](vertex-declaration.md).

Para alguns dados de vértice, a interpolação depende do modo de sombreamento atual, conforme mostrado na tabela a seguir.



| Modo de sombreamento | Descrição                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plano         | Somente o fator de nevoeiro é interpolado no modo de sombreamento simples. Para todos os outros valores interpolados, a cor do primeiro vértice no triângulo é aplicada em toda a face. |
| Gouraud      | A interpolação linear é executada entre todos os três vértices.                                                                                                               |



 

As cores difusas e realces especulares são tratados de forma diferente, dependendo do modelo de cor. No modelo de cor RGB, o sistema usa os componentes de cor vermelha, verde e azul na interpolação.

O componente alfa de uma cor é tratado como um valor interpolado separado porque drivers de dispositivo podem implementar transparência de duas maneiras diferentes: utilizando uma mesclagem de textura ou usando textura pontilhada.

Use o membro ShadeCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar a quais formas de interpolação o driver de dispositivo atual oferece suporte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenar sistemas e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



