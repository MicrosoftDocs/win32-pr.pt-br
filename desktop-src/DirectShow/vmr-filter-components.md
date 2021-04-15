---
description: Componentes de filtro do VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componentes de filtro do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506013"
---
# <a name="vmr-filter-components"></a>Componentes de filtro do VMR

O VMR emprega um design modular que permite aos aplicativos configurá-lo para vários cenários de renderização diferentes. Dependendo de sua configuração, o VMR contém de dois a cinco subcomponentes (além de seus PINs de entrada).

![VMR no modo de janela com vários fluxos](images/vmr-multiple-streams.png)

**Mixer:** O Mixer é um objeto COM responsável por misturar vários fluxos. O desentrelaçamento também ocorre dentro do mixer. O Mixer é carregado pelo VMR quando vários fluxos de entrada são detectados ou quando o vídeo de entrada é entrelaçado. O mixer coleta informações sobre cada fluxo de entrada e classifica os fluxos na ordem Z correta. Ele é responsável por determinar quando cada PIN de entrada recebe um exemplo e para instruir o compositor da imagem no momento adequado para executar a mistura real. O mixer também calcula o carimbo de data/hora a ser aplicado a cada imagem de saída. Quando o aplicativo está fornecendo um bitmap a ser exibido na parte superior da imagem compostada, o Mixer é responsável por garantir que o bitmap seja exibido na parte superior, mesmo que a ordem Z dos fluxos de entrada seja modificada.

**Compositor da imagem:** O compositor da imagem é um objeto COM que executa a mistura real dos fluxos de entrada em uma única superfície do DirectDraw ou do Direct3D fornecida pelo alocador de dados. O VMR fornece um compositor de imagem padrão que permite que os aplicativos executem efeitos de mesclagem alfa 2-D. Os aplicativos podem fornecer um compositor de imagem personalizada para habilitar outros efeitos 2D e 3, como aplicar texturas a partes da imagem, mesclagem alfa por pixel, mapeando a imagem para objetos de 3D ou movendo-D e assim por diante.

**Alocador-apresentador:** O alocador-Presenter é um objeto COM que aloca o objeto DirectDraw ou Direct3D e manipula a comunicação com a placa gráfica. O desenho pode ser executado como um flip ou como um blit. Você pode conectar seu próprio apresentador de alocador para criar e controlar o objeto DirectDraw ou Direct3D e/ou para obter acesso aos bits de vídeo no momento da apresentação.

**Gerenciador de janelas:** O Gerenciador de janelas é usado apenas no modo de janela. O Gerenciador de janelas dá suporte às interfaces herdadas [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) para compatibilidade com versões anteriores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o processamento de mixagem de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



