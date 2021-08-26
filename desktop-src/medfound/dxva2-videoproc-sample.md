---
description: Mostra como usar o processamento de vídeo DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Exemplo de DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc4be1bad6a3955af255cb083a4595ecedfd30
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473922"
---
# <a name="dxva2_videoproc-sample"></a>Exemplo de VideoProc de DXVA2 \_

Mostra como usar o [processamento de vídeo DXVA](dxva-video-processing.md).

Este exemplo gera por meio de programação um vídeo com um fluxo primário e um subfluxo. O fluxo primário exibe as barras de cores SMPTE e o Subfluxo é um retângulo semitransparente. O vídeo é então processado e exibido usando um processador de vídeo DXVA. O usuário pode alterar os valores alfa planar, retângulos de origem e de destino, ajustes de cor e espaço de cores.

![captura de tela do \- exemplo de videoproc de dxva2](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de DXVA:

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Uso

o exemplo de VideoProc de DXVA2 \_ cria um aplicativo Windows.

Opções de linha de comando:



| Opção | Descrição                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Força o aplicativo a usar um dispositivo Direct3D de hardware e um dispositivo de hardware DXVA. |
| -HS    | Força o aplicativo a usar um dispositivo Direct3D de hardware e um dispositivo de DXVA de software. |
| -ss    | Força o aplicativo a usar um dispositivo Direct3D de software e um dispositivo de DXVA de software. |



 

Comandos de teclado:



| Chave       | Descrição                                             |
|-----------|---------------------------------------------------------|
| ALT+ENTER | Alternar entre o modo de janela e o modo de tela inteira.      |
| F1 – F8     | Insira um dos modos mostrados na tabela a seguir.    |
| END       | Habilitar ou desabilitar o registro em log de depuração de quadros descartados. |
| HOME      | Redefina um parâmetro para seu valor inicial.                 |



 

Cada uma das teclas de função F1 a F8 alterna para um modo no qual as teclas de seta podem ser usadas para ajustar um determinado parâmetro de renderização. Além disso, a cor do Subfluxo é alterada.




| Chave | Descrição | 
|-----|-------------|
| F1 | Ajuste os valores Alfa.<br /><ul><li>UP: aumentar o planar de ambos os fluxos.</li><li>Para baixo: diminua a alfa do planar de ambos os fluxos.</li><li>RIGHT: aumentar o pixel alfa do Subfluxo.</li><li>ESQUERDA: diminuir o pixel alfa do Subfluxo.</li></ul>Cor do Subfluxo: branco<br /> | 
| F2 | Ajuste a área de origem do fluxo primário (zoom).<br /><ul><li>UP: aumentar verticalmente (ampliar).</li><li>Para baixo: diminuir verticalmente (reduzir).</li><li>DIREITA: aumentar horizontalmente (ampliar).</li><li>ESQUERDA: diminuir horizontalmente (reduzir).</li></ul>Cor do Subfluxo: vermelho<br /> | 
| F3 | Mova a área de origem do fluxo primário.<br /><ul><li>UP: mover para cima.</li><li>Para baixo: mover para baixo.</li><li>DIREITA: mover para a direita.</li><li>ESQUERDA: mover para a esquerda.</li></ul>Cor do Subfluxo: amarelo<br /> | 
| F4 | Ajuste a área de destino do fluxo principal.<br /><ul><li>UP: aumentar verticalmente.</li><li>Para baixo: diminuir verticalmente.</li><li>DIREITA: aumentar horizontalmente.</li><li>ESQUERDA: diminuir horizontalmente.</li></ul>Cor do Subfluxo: verde<br /> | 
| F5 | Mova a área de destino do fluxo primário.<br /><ul><li>UP: mover para cima.</li><li>Para baixo: mover para baixo.</li><li>DIREITA: mover para a direita.</li><li>ESQUERDA: mover para a esquerda.</li></ul>Cor do Subfluxo: ciano<br /> | 
| F6 | Alterar a cor do plano de fundo ou o espaço de cores.<br /><ul><li>Para cima, para baixo: Percorra os espaços de cores.</li><li>DIREITA, esquerda: percorrer as cores do plano de fundo.</li></ul>Cor do Subfluxo: azul<br /> | 
| F7 | Ajustar o brilho e o contraste.<br /><ul><li>UP: aumentar o brilho.</li><li>Para baixo: diminuir o brilho.</li><li>DIREITA: aumentar contraste.</li><li>ESQUERDA: diminuir contraste.</li></ul>Cor do Subfluxo: magenta<br /> | 
| F8 | Ajuste o matiz e a saturação.<br /><ul><li>UP: aumentar o matiz.</li><li>Para baixo: diminuir o matiz.</li><li>DIREITA: aumentar a saturação.</li><li>ESQUERDA: diminuir a saturação.</li></ul>Cor do Subfluxo: preto<br /> | 




 

Em cada modo, pressionar a tecla HOME redefine os parâmetros para esse modo para seus valores iniciais.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no repositório [Windows github de exemplos clássicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Processamento de vídeo DXVA](dxva-video-processing.md)
</dt> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




