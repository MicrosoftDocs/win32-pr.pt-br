---
title: Recursos de desenho de hardware
description: Recursos de desenho de hardware
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- VCM (Gerenciador de compactação de vídeo), desenho
- VCM (Gerenciador de compactação de vídeo), desenho
- Função ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005619"
---
# <a name="hardware-drawing-capabilities"></a>Recursos de desenho de hardware

Alguns renderizadores podem desenhar diretamente no hardware de vídeo à medida que descompactam quadros de vídeo. Esses renderizadores retornam o \_ sinalizador de desenho VIDCF em resposta à função [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Ao usar esse tipo de processador, seu aplicativo não precisa lidar com os dados descompactados. Ele permite que o renderizador Mantenha os dados descompactados para desenho.

Se seu aplicativo usa um processador com recursos de desenho, ele deve lidar com as seguintes tarefas:

-   Selecione um renderizador.
-   Especifique os formatos de imagem.
-   Inicialize o renderizador.
-   Desenhe os dados.
-   Controlar parâmetros de desenho.

## <a name="renderer-selection"></a>Seleção de renderizador

A macro [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) abre um processador que pode desenhar imagens com o formato especificado. Ele retornará um identificador de um renderizador se for bem-sucedido ou nenhum outro. Essa macro usa a função [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) para abrir o processador.

## <a name="specifying-image-formats"></a>Especificando formatos de imagem

Como seu aplicativo não precisa desenhar os dados descompactados, ele não requer um formato de saída específico. No entanto, deve-se garantir que o renderizador possa desenhar usando o formato de entrada usando a mensagem de [**\_ \_ consulta de desenho ICM**](icm-draw-query.md) (ou use a macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) ). Esta mensagem não pode determinar se um renderizador pode desenhar um bitmap. Se seu aplicativo precisar determinar se o renderizador pode desenhar o bitmap, use essa mensagem com a função [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) .

Seu aplicativo pode ter um processador sugira um formato de entrada usando a função [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) . Essa função é usada quando um renderizador separa os recursos de desenho dos recursos de descompactação. A maioria dos aplicativos que usam as funções de desenho não precisará determinar o formato de saída.

## <a name="renderer-initialization"></a>Inicialização do processador

A função [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) Inicializa um renderizador e informa o destino do desenho. Essa função também pode executar as seguintes tarefas:

-   Determine se o renderizador oferece suporte a um formato de entrada específico.
-   Especifique se a operação de desenho ocupa uma janela ou toda a tela.
-   Especifique a parte da imagem a ser exibida usando o retângulo de origem.
-   Defina a taxa de reprodução da sequência de imagens.

Alguns renderizadores armazenam em buffer os dados compactados para operar com mais eficiência. Seu aplicativo pode enviar a [**mensagem \_ GETBUFFERSWANTED do ICM**](icm-getbufferswanted.md) (ou usar a macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) ) para determinar o número de buffers que o processador solicita. Seu aplicativo deve pré-carregar esses buffers e enviá-los para o renderizador antes do desenho.

## <a name="drawing-the-data"></a>Desenhando os dados

Você pode usar a função [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) para descompactar os dados para desenho. O renderizador, no entanto, não inicia o desenho de dados até que seu aplicativo envie a mensagem de [**\_ \_ início do ICM Draw**](icm-draw-start.md) (ou usa a macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) ). Quando o aplicativo chama essa função, o renderizador começa a desenhar os quadros na taxa especificada pelo parâmetro *dwRate* dividido pelo parâmetro *dwScale* ; esses parâmetros foram fornecidos quando o aplicativo inicializava o renderizador usando a função [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) . O desenho continua até que seu aplicativo envie a mensagem de [**\_ \_ parada ICM Draw**](icm-draw-stop.md) (ou usa a macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) ).

> [!Note]  
> Se um renderizador armazenar os dados em buffer antes do desenho, seu aplicativo não deverá usar a macro **ICDrawStart** até que tenha enviado o número de quadros retornado pelo renderizador para a macro **ICGetBuffersWanted** .

 

O parâmetro *lTime* de [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) especifica o tempo para desenhar um quadro. O renderizador divide esse inteiro pela escala de tempo especificada com [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) para obter a hora real. Os horários para as funções **ICDraw** são relativos a **ICDrawStart**. **ICDrawStart** define o relógio como zero. Por exemplo, se seu aplicativo especificar 1000 para a escala de tempo e 75 para *lTime*, o renderizador desenhará o quadro de 75 milissegundos na sequência.

## <a name="controlling-drawing-parameters"></a>Controlando parâmetros de desenho

Você pode monitorar o relógio de um processador enviando a mensagem [**do \_ ICM \_ draw getTime**](icm-draw-gettime.md) (ou usar a macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) ) e pode definir o relógio de um processador que pode desenhar dados enviando a mensagem [**\_ \_ setTime do ICM Draw**](icm-draw-settime.md) (ou usar a macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) ).

Para alterar a posição atual enquanto um renderizador está desenhando, seu aplicativo pode enviar a mensagem de [**\_ \_ janela de desenho ICM**](icm-draw-window.md) (ou usar a macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) ) para reposicionar a janela. Normalmente, os aplicativos usam essa mensagem sempre que a janela é alterada.

Se a janela de reprodução obtiver uma mensagem de paleta de percepção, seu aplicativo deverá enviar a mensagem de [**\_ \_ percepção de desenho ICM**](icm-draw-realize.md) (ou usar a macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) ) para que o renderizador perceba a paleta novamente para reprodução. Os aplicativos podem alterar a paleta enviando a mensagem [**ICM \_ draw \_ CHANGEPALETTE**](icm-draw-changepalette.md) (ou usar a macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) ) e obter a paleta atual enviando a mensagem [**ICM \_ extrair \_ a \_ paleta**](icm-draw-get-palette.md) .

Alguns renderizadores devem ser especificamente instruídos para exibir os quadros passados a eles. Enviar a mensagem de [**\_ desenho \_ RENDERBUFFER do ICM**](icm-draw-renderbuffer.md) (ou usar a macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) ) faz com que esses renderizadores desenhem o quadro.

 

 




