---
description: Modo de mixagem YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modo de mixagem YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829572"
---
# <a name="yuv-mixing-mode"></a>Modo de mixagem YUV

Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.

A partir do Windows XP Service Pack 2, o VMR dá suporte a um modo de combinação chamado modo de mixagem de YUV. Esse modo é mais útil para aplicativos avançados de TV ou DVD. Ele negocia parte do poder do mixer do VMR para melhorar o desempenho em hardware de gráficos de baixo nível que usa um design de arquitetura de memória unificada. O modo de mixagem de YUV tem suporte no VMR-7 e no VMR-9.

**Vantagens**

O modo de mixagem YUV tem várias vantagens relacionadas ao desempenho de renderização sobre o modo de mixagem RGB original com suporte no VMR:

-   Quando o VMR está no modo de mistura YUV, todas as operações de composição de fluxo de vídeo e desentrelaçamento são executadas no espaço de cores YUV. As superfícies YUV geralmente exigem de 50% a 60% menos largura de banda de memória do que as superfícies RGB equivalentes.
-   A composição de desentrelaçamento e de fluxo são executadas por uma única chamada para o driver de gráficos. O driver pode usar os recursos texturing do hardware de gráficos, resultando em mais economia de largura de banda de memória.

Embora qualquer aplicativo de vídeo possa usar o modo de mixagem YUV, ele destina-se principalmente a dois tipos de aplicativo de reprodução de vídeo:

1.  Aplicativos de TV que exibem legendas codificadas ou teletexto.
2.  Os aplicativos de DVD exibem dados de subimagem de DVD ou legendas codificadas.

**Restrições**

Várias restrições são impostas pelo VMR quando ele é colocado no modo de mixagem YUV:

-   O fluxo 0 (o fluxo conectado ao pino de entrada 0) pode ser progressivo ou entrelaçado; todos os outros fluxos devem ser progressivos.
-   GUID \_ NULL (modo de weave) não é permitido para o fluxo 0.
-   DeinterlacePref \_ weave não pode ser usada como um modo de fallback porque isso pode impedir que um dispositivo de desentrelaçamento seja criado. O modo de mixagem YUV requer um dispositivo de desentrelaçamento, mesmo se o vídeo de entrada não estiver entrelaçado.
-   Nenhuma alteração pode ser feita no valor alfa do planar associado a cada fluxo de entrada do VMR.
-   O usuário não pode alterar a ordem Z dos fluxos de vídeo conectados. A ordem Z padrão é retirada da ordem do PIN.
-   Não há suporte para o chaveamento de cor.
-   O pino de entrada 0 deve receber o fluxo de vídeo.
-   Os outros Pins de entradas só podem receber dados de Subfluxo de vídeo, como subimagem de DVD, legendas codificadas ou teletexto.
-   Os outros Pins de entradas só podem aceitar formatos de YUV alfa por pixel, como AYUV, AI44 e IA44.
-   Nenhum dos Pins de entrada do VMR pode aceitar todos os formatos RGB.
-   Imagens de bitmap fornecidas pelo aplicativo não podem mais ser combinadas com o vídeo antes da apresentação para a exibição.
-   Os subfluxos individuais não podem ser invertidos horizontal ou verticalmente usando as funções do mixer "retângulo de saída" do VMR. Há suporte para o redimensionamento de fluxo "normal" e redimensionar.
-   A cor do plano de fundo de mistura (especificada por [**IVMRMixerControl:: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) ainda é especificada no espaço de cores RGB, assim como no modo de mistura RGB.

**Configuration**

Os aplicativos devem configurar explicitamente o VMR para tirar proveito do modo de mixagem YUV; o modo de mixagem RGB original permanece o modo de combinação padrão. Para habilitar o modo de mixagem YUV no VMR-7, chame [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) com o \_ sinalizador MixerPref RenderTargetYUV. Essa chamada deve ser feita antes que qualquer um dos Pins de entrada do VMR esteja conectado. Para habilitar o modo de mixagem YUV no VMR-9, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o \_ sinalizador MixerPref9 RenderTargetYUV.

A única maneira de determinar se o VMR-7 dá suporte ao novo modo de mixagem YUV é tentar configurar o VMR nesse modo. Se a chamada for realizada com sucesso, você ainda poderá colocar o VMR novamente no modo de mistura RGB, se necessário. Depois que ele é definido no modo de mistura YUV, o VMR só pode ser alterado para o modo de mistura RGB depois que todos os Pins de entrada tiverem sido desconectados.

No modo de mixagem YUV, você pode reduzir a carga na GPU (unidade de processamento gráfico) aplicando os seguintes sinalizadores no método **SetMixingPrefs** :



| Sinalizador                                                                                 | Descrição                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB<br/> | Mude para Bob desentrelaçar.                                     |
| VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2<br/>  | DECIMATE a imagem por um fator de 2 na horizontal e na vertical. |



 

Você pode adicionar ou remover esses sinalizadores enquanto o grafo de filtro está em execução; a alteração é aplicada quando o mixer do VMR compõe o próximo quadro de vídeo. Os sinalizadores não são mutuamente exclusivos. Essas configurações reduzem a qualidade da imagem, portanto, normalmente você as aplicaria somente quando a qualidade do vídeo for menos importante — por exemplo, se o vídeo estiver sendo reproduzido em uma pequena parte da interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




