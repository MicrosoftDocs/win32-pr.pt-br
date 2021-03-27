---
description: Um espaço de coordenadas é um espaço planar baseado no sistema de coordenadas cartesianas.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Transformação de espaços de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1bca3d7190c4566ea7548166134ff745cc5e2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837441"
---
# <a name="transformation-of-coordinate-spaces"></a>Transformação de espaços de coordenadas

Um *espaço de coordenadas* é um espaço planar baseado no sistema de coordenadas cartesianas. Esse sistema fornece um meio de especificar o local de cada ponto em um plano. Ele requer dois eixos que são perpendiculares e iguais em comprimento. A ilustração a seguir mostra um espaço de coordenadas.

![ilustração de um espaço de coordenadas, mostrando a origem, ambos os eixos e os valores máximo e mínimo de cada eixo](images/cstrn-07.png)

O sistema dá suporte a quatro espaços de coordenadas, conforme descrito na tabela a seguir.



| Espaço de coordenadas | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Usado opcionalmente como o espaço de coordenadas inicial para transformações gráficas. Ele permite o dimensionamento, a tradução, a rotação, a distorção e a reflexão. O espaço de mundo mede 2 ^ 32 unidades de altura em 2 ^ 32 unidades de largura.                                                                                                                                                                                                                                                                |
| página             | Usado como o próximo espaço após o espaço do mundo ou como o espaço inicial para transformações gráficas. Ele define o modo de mapeamento. O espaço de página também mede 2 ^ 32 unidades de altura em 2 ^ 32 unidades de largura.                                                                                                                                                                                                                                                                              |
| dispositivo           | Usado como o próximo espaço após o espaço da página. Ele permite apenas a tradução, o que garante que a origem do espaço do dispositivo seja mapeada para o local apropriado no espaço físico do dispositivo. O espaço do dispositivo mede 2 ^ 27 unidades de altura em 2 ^ 27 unidades de largura.                                                                                                                                                                                                                                          |
| dispositivo físico  | O espaço final (saída) para transformações gráficas. Geralmente, ele se refere à área do cliente da janela do aplicativo; no entanto, ele também pode incluir toda a área de trabalho, uma janela completa (incluindo o quadro, a barra de título e a barra de menus) ou uma página de papel de impressora ou plotadora, dependendo da função que obteve o identificador para o contexto do dispositivo. As dimensões do dispositivo físico variam de acordo com as dimensões definidas pela tecnologia de exibição, impressora ou plotadora. |



 

O espaço de página funciona com espaço de dispositivo para fornecer aplicativos com unidades independentes de dispositivo, como milímetros e polegadas. Esta visão geral refere-se ao espaço do mundo e ao espaço da página como espaço lógico.

Para representar a saída em um dispositivo físico, o sistema copia (ou mapeia) uma região retangular de um espaço de coordenadas para o próximo usando uma transformação até que a saída apareça em sua totalidade no dispositivo físico. O mapeamento começa no espaço do mundo do aplicativo se o aplicativo tiver chamado a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ; caso contrário, o mapeamento ocorrerá no espaço da página. Como o sistema copia cada ponto dentro da região retangular de um espaço para outro, ele aplica um algoritmo chamado transformação. Uma *transformação* altera (ou transforma) o tamanho, a orientação e a forma dos objetos que são copiados de um espaço de coordenadas para outro. Embora uma transformação afete um objeto como um todo, ela é aplicada a cada ponto, ou a cada linha, no objeto.

A ilustração a seguir mostra uma transformação típica executada usando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .

![ilustração que mostra um retângulo que altera o tamanho e a posição conforme ele aparece no espaço do mundo, espaço de página, espaço do dispositivo e dispositivo](images/cstrn-08.png)

 

 



