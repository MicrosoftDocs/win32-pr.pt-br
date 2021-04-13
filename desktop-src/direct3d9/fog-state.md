---
description: Os efeitos de neblina podem dar uma cena 3D maior realm.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Estado de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370035"
---
# <a name="fog-state-direct3d-9"></a>Estado de neblina (Direct3D 9)

Os efeitos de neblina podem dar uma cena 3D maior realm. Você pode usar efeitos de neblina para mais do que simular a neblina. Eles também podem diminuir a clareza de uma cena com distância. Isso espelha o que acontece no mundo real; à medida que os objetos se tornam mais distantes do usuário, seus detalhes são menos distintos.

Para obter mais informações sobre como usar a neblina em seu aplicativo, consulte [neblina (Direct3D 9)](fog.md).

Um aplicativo C++ controla a neblina por meio de Estados de renderização de dispositivo. O tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) inclui Estados para controlar se pixel (tabela) ou sombra de vértice é usado, qual cor é, a fórmula de neblina que o sistema aplica e os parâmetros da fórmula.

Você habilita a neblina definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGENABLE como **true**. A cor de neblina pode ser definida como qualquer valor de cor usando o \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR; o componente alfa da cor de neblina é ignorado.

Os \_ Estados de RENDERIZAÇÃO D3DRS FOGTABLEMODE e D3DRS \_ FOGVERTEXMODE controlam a fórmula de neblina aplicada para cálculos de neblina e controlam indiretamente qual tipo de neblina é aplicado. Ambos os Estados de processamento podem ser definidos como um membro do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) . A configuração de Process State como D3DFOG \_ None desabilita a sombra de pixel ou Vertex, respectivamente. Se ambos os Estados de renderização estiverem definidos como modos válidos, o sistema aplicará apenas efeitos de neblina de pixel.

Os Estados de renderização de D3DRS \_ FOGSTART e D3DRS \_ FOGEND do controle de parâmetros de fórmulas de neblina para o modo de D3DFOG \_ linear. Os controles de estado de renderização de D3DRS FOGDENSITY são uma \_ densidade de neblina nos modos de neblina exponencial.

Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
