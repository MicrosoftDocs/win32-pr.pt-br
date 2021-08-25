---
description: Mostra como usar o Processamento de Vídeo DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fda9829398b97e7670bb2d1f8cc076c00cda77e1ad06131603603f6f49191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828277"
---
# <a name="dxva2_videoproc-sample"></a>Exemplo de VideoProc DXVA2 \_

Mostra como usar o [Processamento de Vídeo DXVA.](dxva-video-processing.md)

Este exemplo gera programaticamente um vídeo com um fluxo primário e um substream. O fluxo primário exibe barras de cores SMPTE e o substream é um retângulo semi-transparente. Em seguida, o vídeo é processado e exibido usando um processador de vídeo DXVA. O usuário pode alterar os valores alfa planar, os retângulos de origem e de destino, os ajustes de cor e o espaço de cores.

![captura de tela do exemplo de \- videoproc dxva2](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces DXVA:

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Uso

O exemplo DXVA2 \_ VideoProc cria um Windows aplicativo.

Opções de linha de comando:



| Opção | Descrição                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Força o aplicativo a usar um dispositivo Direct3D de hardware e um dispositivo DXVA de hardware. |
| -hs    | Força o aplicativo a usar um dispositivo Direct3D de hardware e um dispositivo DXVA de software. |
| -ss    | Força o aplicativo a usar um dispositivo Direct3D de software e um dispositivo DXVA de software. |



 

Comandos de teclado:



| Chave       | Descrição                                             |
|-----------|---------------------------------------------------------|
| ALT+ENTER | Alternar entre o modo de janela e o modo de tela inteira.      |
| F1 –F8     | Insira um dos modos mostrados na tabela a seguir.    |
| END       | Habilitar ou desabilitar o log de depuração para quadros descartados. |
| HOME      | Redefinir um parâmetro para seu valor inicial.                 |



 

Cada uma das teclas de função F1 a F8 muda para um modo no qual as teclas de direção podem ser usadas para ajustar um parâmetro de renderização específico. Além disso, a cor do substream muda.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Chave</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>F1</td>
<td>Ajuste os valores alfa.<br/>
<ul>
<li>UP: aumente o alfa planar de ambos os fluxos.</li>
<li>DOWN: diminua o alfa planar de ambos os fluxos.</li>
<li>RIGHT: aumente o pixel alfa do substream.</li>
<li>LEFT: diminua o alfa de pixel do substream.</li>
</ul>
Cor do substream: Branco<br/></td>
</tr>
<tr class="even">
<td>F2</td>
<td>Ajuste a área de origem do fluxo primário (zoom).<br/>
<ul>
<li>UP: aumente verticalmente (ampliar).</li>
<li>DOWN: diminua verticalmente (reduzir).</li>
<li>DIREITA: aumentar horizontalmente (ampliar).</li>
<li>LEFT: diminua horizontalmente (reduzir).</li>
</ul>
Cor do substream: Vermelho<br/></td>
</tr>
<tr class="odd">
<td>F3</td>
<td>Mova a área de origem do fluxo primário.<br/>
<ul>
<li>UP: mova para cima.</li>
<li>DOWN: mova para baixo.</li>
<li>DIREITA: mova para a direita.</li>
<li>LEFT: mova para a esquerda.</li>
</ul>
Cor do substream: amarelo<br/></td>
</tr>
<tr class="even">
<td>F4</td>
<td>Ajuste a área de destino do fluxo primário.<br/>
<ul>
<li>UP: aumente verticalmente.</li>
<li>DOWN: diminua verticalmente.</li>
<li>DIREITA: aumente horizontalmente.</li>
<li>LEFT: diminua horizontalmente.</li>
</ul>
Cor do substream: Verde<br/></td>
</tr>
<tr class="odd">
<td>F5</td>
<td>Mova a área de destino do fluxo primário.<br/>
<ul>
<li>UP: mova para cima.</li>
<li>DOWN: mova para baixo.</li>
<li>DIREITA: mova para a direita.</li>
<li>LEFT: mova para a esquerda.</li>
</ul>
Cor do substream: Ciano<br/></td>
</tr>
<tr class="even">
<td>F6</td>
<td>Altere a cor da tela de fundo ou o espaço de cor.<br/>
<ul>
<li>UP, DOWN: ciclo pelos espaços de cores.</li>
<li>RIGHT, LEFT: passa pelas cores da plano de fundo.</li>
</ul>
Cor do substream: azul<br/></td>
</tr>
<tr class="odd">
<td>F7</td>
<td>Ajuste o brilho e o contraste.<br/>
<ul>
<li>UP: aumentar o brilho.</li>
<li>DOWN: diminua o brilho.</li>
<li>RIGHT: aumentar o contraste.</li>
<li>LEFT: diminua o contraste.</li>
</ul>
Cor do substream: Magenta<br/></td>
</tr>
<tr class="even">
<td>F8</td>
<td>Ajuste matiz e saturação.<br/>
<ul>
<li>UP: aumente o matiz.</li>
<li>DOWN: diminua o matiz.</li>
<li>RIGHT: aumente a saturação.</li>
<li>LEFT: diminua a saturação.</li>
</ul>
Cor do substream: Preto<br/></td>
</tr>
</tbody>
</table>



 

Em cada modo, pressionar a tecla HOME redefine os parâmetros desse modo para seus valores iniciais.

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

 

 




