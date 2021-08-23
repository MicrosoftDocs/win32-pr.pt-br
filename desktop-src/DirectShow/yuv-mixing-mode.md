---
description: Modo de combinação YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modo de combinação YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 957c5345eb80576ad0371558bb60d0b6651221bd98d7830cb968f39c16330fb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290746"
---
# <a name="yuv-mixing-mode"></a>Modo de combinação YUV

Este tópico se aplica ao Windows XP Service Pack 2 ou posterior.

A partir Windows XP Service Pack 2, a VMR dá suporte a um modo de combinação chamado modo de combinação YUV. Esse modo é mais útil para aplicativos avançados de TV ou DVD. Ele troca parte do poder do mixer de VMR para melhorar o desempenho em hardware de gráficos de baixo nível que usa um design de arquitetura de memória unificada. Há suporte para o modo de combinação YUV na VMR-7 e na VMR-9.

**Vantagens**

O modo de combinação YUV tem várias vantagens relacionadas ao desempenho de renderização em relação ao modo de combinação RGB original com suporte da VMR:

-   Quando a VMR está no modo de combinação YUV, todas as operações de desentração e composição de fluxo de vídeo são executadas no espaço de cores YUV. As superfícies YUV normalmente exigem de 50% a 60% menos largura de banda de memória do que superfícies RGB equivalentes.
-   A desinteressação e a composição de fluxo são executadas por uma única chamada para o driver gráfico. O driver pode usar as funcionalidades de texto múltiplo do hardware gráfico, resultando em economias de largura de banda de memória adicionais.

Embora qualquer aplicativo de vídeo possa usar o modo de combinação YUV, ele destina-se principalmente a dois tipos de aplicativo de reprodução de vídeo:

1.  Aplicativos de TV que exibem legendas ou teletextos fechados.
2.  Os aplicativos de DVD exibem dados de subpicture de DVD ou legendas fechadas.

**Restrições**

Várias restrições são impostas pela VMR quando ela é colocada no modo de combinação YUV:

-   O fluxo 0 (o fluxo conectado ao Pino de Entrada 0) pode ser progressivo ou entrelaçado; todos os outros fluxos devem ser progressivos.
-   GUID \_ NULL (modo de weave) não é permitido para o fluxo 0.
-   DeinteriaPref Weave não pode ser usado como um modo de fallback porque isso pode impedir que um dispositivo de \_ intercalação seja criado. O modo de combinação YUV requer um dispositivo deinteressamento mesmo que o vídeo de entrada não seja entrelaçado.
-   Nenhuma alteração pode ser feita no valor alfa planar associado a cada fluxo de entrada de VMR.
-   O usuário não pode alterar a ordem Z dos fluxos de vídeo conectados. A ordem Z padrão é retirada da ordem de pino.
-   Não há suporte para o chaveamento de cores.
-   O pino de entrada 0 deve receber o fluxo de vídeo.
-   Os outros pinos de entrada só podem receber dados de sub-fluxo de vídeo, como sub-imagem de DVD, legendas fechadas ou teletexto.
-   As outras entradas só podem aceitar formatos YUV alfa por pixel, como AYUV, AI44 e IA44.
-   Nenhum dos pinos de entrada da VMR pode aceitar nenhum formato RGB.
-   As imagens de bitmap fornecidas pelo aplicativo não podem mais ser combinadas com o vídeo antes da apresentação para a exibição.
-   Sub-fluxos individuais não podem ser invertidos horizontal ou verticalmente usando as funções de "retângulo de saída" do mixer da VMR. Há suporte para reposicionamento e rees tamanho do fluxo "Normal".
-   A cor da tela de fundo de combinação (especificada por [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) ainda é especificada no espaço de cores RGB, assim como no modo de combinação RGB.

**Configuration**

Os aplicativos devem configurar explicitamente a VMR para aproveitar o modo de combinação YUV; O modo de combinação RGB original permanece o modo de combinação padrão. Para habilitar o modo de combinação YUV na VMR-7, chame [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) com o sinalizador MixerPref \_ RenderTargetYUV. Essa chamada deve ser feita antes que qualquer um dos pinos de entrada da VMR seja conectado. Para habilitar o modo de combinação YUV na VMR-9, chame [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o sinalizador MixerPref9 \_ RenderTargetYUV.

A única maneira de determinar se a VMR-7 dá suporte ao novo modo de combinação YUV é tentar configurar a VMR nesse modo. Se a chamada for bem-sucedida, você ainda poderá colocar a VMR de volta no modo de combinação RGB, se necessário. Depois de definida no modo de combinação YUV, a VMR só poderá ser alterada de volta para o modo de combinação RGB depois que todos os pinos de entrada foram desconectados.

No modo de combinação YUV, você pode reduzir a carga na GPU (unidade de processamento gráfico) aplicando os seguintes sinalizadores no **método SetMixingPrefs:**



| Sinalizador                                                                                 | Descrição                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB<br/> | Alternar para desintercalação de bob.                                     |
| VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2<br/>  | Dizima a imagem por um fator de 2 horizontal e verticalmente. |



 

Você pode adicionar ou remover esses sinalizadores enquanto o grafo de filtro está em execução; a alteração é aplicada quando o mixer de VMR compõe o próximo quadro de vídeo. Os sinalizadores não são mutuamente exclusivos. Essas configurações reduzem a qualidade da imagem, portanto, normalmente, você as aplicaria somente quando a qualidade do vídeo fosse menos importante, por exemplo, se o vídeo estivesse sendo gravado em uma pequena parte da interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de combinação de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




