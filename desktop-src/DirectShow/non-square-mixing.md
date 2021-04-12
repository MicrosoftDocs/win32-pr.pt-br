---
description: Mixagem não quadrada
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Mixagem não quadrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500550"
---
# <a name="non-square-mixing"></a>Mixagem não quadrada

Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.

Quando o VMR-9 combina dois ou mais fluxos, há dois pontos em que o dimensionamento pode ocorrer: quando o mixer compõe os fluxos de entrada e quando o alocador de dados renderiza a imagem composta.

![operações de mixagem do VMR](images/vmr-nonsquare-mixing.png)

As versões anteriores do VMR-9 sempre compõevam os fluxos de entrada usando uma taxa de proporção de pixel (PAR) quadrado (1:1), mesmo quando havia apenas um fluxo de vídeo único. Se o fluxo de entrada tiver pixels não quadrados, isso causaria uma operação de dimensionamento desnecessária. O dimensionamento deve ser evitado o máximo possível, é claro, porque ele degrada a qualidade final da imagem.

A partir do Windows XP Service Pack 2, o VMR-9 dá suporte a duas maneiras diferentes de evitar o problema de dimensionamento duplo:

-   Implemente um apresentador de alocador personalizado e dê suporte à interface [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .
-   Use o modo de combinação não quadrado.

Esta seção descreve o modo de mistura não quadrada. Os aplicativos podem combinar as duas técnicas.

**Como funciona a mistura não quadrada**

No modo de mistura não-quadrada, o VMR-9 seleciona um fluxo de entrada para ser o tamanho e o PAR de destino. O mixer do VMR não dimensiona o vídeo do fluxo ou de quaisquer outros fluxos com o mesmo tamanho de imagem e PAR. Fluxos com um tamanho ou taxa de proporção diferente são dimensionados para corresponder ao PAR de destino e letterboxed para se ajustarem ao tamanho final da imagem de saída.

A escolha dos fluxos depende do modo de combinação atual:

-   O modo de mixagem YUV é restrito a um fluxo de vídeo no pino 0. (Os outros Pins podem ter fluxos de subimagem ou legenda oculta.) Portanto, o VMR-9 sempre seleciona o pino 0 para o tamanho da imagem de destino e PAR.
-   No modo de mixagem RGB, o VMR seleciona o fluxo com o maior tamanho de imagem. Se houver mais de um, ele selecionará aquele com a ordem z mais alta; e se ainda houver um vínculo, ele selecionará o fluxo com o número de PIN mais baixo.

**Exemplos de operação**

**Exemplo 1.** O fluxo 0 é 720 x 480 pixels com uma taxa de proporção de imagem de 16:9. O fluxo 1 é um 640 x 480 pixels com uma taxa de proporção de imagem de 4:3.

Neste exemplo, o fluxo 0 tem o maior tamanho de imagem, portanto, o VMR escolhe esse fluxo, independentemente do modo de mistura RGB ou do modo de combinação de YUB. O PAR é 32:27 (16:9/720:480), o que significa que a imagem deve ser esticada horizontalmente por essa proporção para produzir a taxa de proporção de imagem 16:9 correta.

Para corresponder ao PAR de destino, o mixer do VMR dimensiona o fluxo 1 pela taxa inversa (27:32), resultando em uma imagem 540 x 480. Os dois fluxos são então compostos em uma superfície. Para exibir a imagem resultante corretamente, o apresentador de alocador deve alongar a imagem horizontalmente para se ajustar à taxa de proporção da imagem 16:9.

![exemplo 1.](images/vmr-nonsquare-mixing2.png)

**Exemplo 2.** O fluxo 0 é 720 x 480 pixels com uma taxa de proporção de imagem de 16:9. O fluxo 1 é um 1024 x 768 pixels com uma taxa de proporção de imagem de 4:3.

Se o VMR-9 estiver usando o modo de mixagem YUV, ele sempre selecionará o fluxo 0. Portanto, ele amplia o fluxo de 1 a 540 x 480 pixels, para corresponder ao PAR do fluxo 0.

Se o VMR-9 estiver usando o modo de mixagem RGB, ele selecionará o fluxo 1 como o destino, pois esse fluxo tem o maior tamanho de imagem. Ele amplia o fluxo 0 para um tamanho de imagem de 1024 x 576 pixels. Observe que, nesse caso, a imagem compostada tem um PAR de 1:1, portanto, o alocador-apresentador não precisa corrigir para pixels não quadrados. (Talvez ainda precise ampliar o vídeo para considerar o retângulo de destino.)

**Usando o modo de combinação não quadrado**

O modo de mixagem não quadrado é recomendado se qualquer uma das condições a seguir for verdadeira:

-   Seu aplicativo nunca envia mais de um fluxo de vídeo para o VMR-9.
-   Seu aplicativo processa arquivos de DVD, televisão ou MS-DVR. Você também deve usar o modo de mixagem YUV nesse caso, se o hardware de gráficos oferecer suporte a ele.

Se seu aplicativo misturar vários fluxos de vídeo que podem ter tamanhos de imagem ou proporções de pixel variáveis, o modo de combinação de quadrado padrão é recomendado.

Para configurar o modo de mistura não-quadrado, o grafo de filtro deve ser interrompido e todos os Pins de entrada desconectados no VMR-9. Em seguida, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o \_ sinalizador MixerPref9 NonSquareMixing:


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Se você combinar o \_ sinalizador MixerPref9 NonSquareMixing com o \_ sinalizador MixerPref9 ARAdjustXorY, o VMR-9 ignorará o \_ sinalizador MixerPref9 ARAdjustXorY.

 

Se seu aplicativo usar um apresentador de alocador personalizado com modo de combinação não quadrado, lembre-se de que a imagem compostada pode ter um PAR não quadrado. O apresentador de alocador deve escalar a imagem para um quadrado (1:1) PAR.

**Bitmaps estáticos**

Se você usar a interface [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) para misturar um bitmap estático no vídeo, considere o bitmap para ser um segundo fluxo de vídeo para fins do modo de combinação do VMR.

O VMR trata o bitmap como tendo o mesmo PAR que o destino. Ele não dimensiona o bitmap para ajustar a taxa de proporção de pixel do destino. Na configuração padrão do VMR, o destino tem um PAR de 1:1, que corresponde à maioria dos bitmaps. No modo de mistura não quadrada, o destino pode ter pixels não quadrados. Para garantir que o bitmap seja exibido corretamente, o aplicativo deve fornecer uma imagem cujo PAR corresponda ao PAR de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



