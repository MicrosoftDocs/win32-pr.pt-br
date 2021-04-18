---
description: Para um app renderizar uma cena 3D de forma realista, ele deve considerar o efeito que as fontes de luz tem sobre a aparência da cena.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Mapeamento claro com texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105784635"
---
# <a name="light-mapping-with-textures-direct3d-9"></a>Mapeamento claro com texturas (Direct3D 9)

Para um app renderizar uma cena 3D de forma realista, ele deve considerar o efeito que as fontes de luz tem sobre a aparência da cena. Embora as técnicas como sombreamento simples e de Gouraud sejam ferramentas valiosas nesse sentido, elas podem ser insuficientes para suas necessidades. O Direct3D oferece suporte à passagem múltipla e à mesclagem de textura múltipla. Esses recursos permitem que o app renderize cenas com uma aparência mais realista do que as cenas renderizadas somente com técnicas de sombreamento. Ao aplicar um ou mais mapas de luz, o app pode mapear áreas de luz e sombra nos primitivos.

Um mapa de luz é uma textura ou um grupo de texturas que contém informações sobre a iluminação em uma cena 3D. Você pode armazenar as informações de iluminação nos valores de alfa do mapa de luz, nos valores de cor ou em ambos.

Se você implementar o mapeamento de luz usando a mesclagem de textura de passagem múltipla, o app deve renderizar o mapa de luz nos primitivos na primeira passagem. Ele deve usar uma segunda passada para renderizar a textura base. A exceção é o mapeamento de luz especular. Nesse caso, renderize a textura base primeiro; em seguida, adicione o mapa de luz.

A mistura de textura múltipla permite que o app renderize o mapa de luz e a textura base em uma passagem. Se o hardware do usuário fornece mistura de textura múltipla, o app deve aproveitar isso ao executar o mapeamento de luz. Isso melhora significativamente o desempenho do app.

Com mapas de luz, um app Direct3D pode conseguir uma variedade de efeitos de iluminação ao renderizar primitivos. Ele pode mapear não apenas as luzes monocromáticas e coloridas em uma cena, mas também pode adicionar detalhes como realces especulares e iluminação difusa.

As informações sobre o uso da mistura de textura do Direct3D para executar o mapeamento de luz são apresentadas nos tópicos a seguir.

-   [Mapas leves monocromáticos (Direct3D 9)](monochrome-light-maps.md)
-   [Mapas de luz de cor (Direct3D 9)](color-light-maps.md)
-   [Mapas de luz especulares (Direct3D 9)](specular-light-maps.md)
-   [Mapas de luz difusa (Direct3D 9)](diffuse-light-maps.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de textura](texture-blending.md)
</dt> </dl>

 

 



