---
description: Um espaço de coordenadas é um espaço planar baseado no sistema de coordenadas cartesiano.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Transformação de espaços de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ffaec6a6dab09b841f95f4704048a4145d2b2bd84c232658b2b659d26d37be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965156"
---
# <a name="transformation-of-coordinate-spaces"></a>Transformação de espaços de coordenadas

Um *espaço de coordenadas* é um espaço planar baseado no sistema de coordenadas cartesiano. Esse sistema fornece um meio de especificar o local de cada ponto em um plano. Ele requer dois eixos que são iguais e de comprimento. A ilustração a seguir mostra um espaço de coordenadas.

![ilustração de um espaço de coordenadas, mostrando a origem, ambos os eixos e os valores máximo e mínimo de cada eixo](images/cstrn-07.png)

O sistema dá suporte a quatro espaços de coordenadas, conforme descrito na tabela a seguir.



| Espaço de coordenadas | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Usado opcionalmente como o espaço de coordenadas inicial para transformações gráficas. Ele permite dimensionamento, tradução, rotação, conversão e reflexão. O espaço mundial mede 2^32 unidades de altura por 2^32 unidades de largura.                                                                                                                                                                                                                                                                |
| página             | Usado como o próximo espaço após o espaço do mundo ou como o espaço inicial para transformações gráficas. Ele define o modo de mapeamento. O espaço de página também mede 2^32 unidades de altura por 2^32 unidades de largura.                                                                                                                                                                                                                                                                              |
| dispositivo           | Usado como o próximo espaço após o espaço de página. Ele só permite a tradução, o que garante que a origem do espaço do dispositivo seja mapeada para o local adequado no espaço do dispositivo físico. O espaço do dispositivo mede 2^27 unidades de altura por 2^27 unidades de largura.                                                                                                                                                                                                                                          |
| dispositivo físico  | O espaço final (saída) para transformações gráficas. Geralmente, ele se refere à área de cliente da janela do aplicativo; No entanto, ele também pode incluir toda a área de trabalho, uma janela completa (incluindo o quadro, a barra de título e a barra de menus) ou uma página de papel de impressora ou plotador, dependendo da função que obteve o controle para o contexto do dispositivo. As dimensões do dispositivo físico variam de acordo com as dimensões definidas pela tecnologia de exibição, impressora ou plotador. |



 

O espaço de página funciona com o espaço do dispositivo para fornecer aos aplicativos unidades independentes de dispositivo, como milímetros e polegadas. Esta visão geral refere-se ao espaço do mundo e ao espaço de página como espaço lógico.

Para representar a saída em um dispositivo físico, o sistema copia (ou mapeia) uma região retangular de um espaço de coordenadas para o próximo usando uma transformação até que a saída apareça inteiramente no dispositivo físico. O mapeamento começará no espaço mundial do aplicativo se o aplicativo tiver chamado a [**função SetWorldTransform;**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) caso contrário, o mapeamento ocorrerá no espaço da página. À medida que o sistema copia cada ponto dentro da região retangular de um espaço para outro, ele aplica um algoritmo chamado transformação. Uma *transformação* altera (ou transforma) o tamanho, a orientação e a forma dos objetos copiados de um espaço de coordenadas para outro. Embora uma transformação afete um objeto como um todo, ela é aplicada a cada ponto, ou a cada linha, no objeto .

A ilustração a seguir mostra uma transformação típica executada usando a [**função SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)

![ilustração mostrando um retângulo que altera o tamanho e a posição conforme ele aparece no espaço do mundo, no espaço de página, no espaço do dispositivo e no dispositivo](images/cstrn-08.png)

 

 



