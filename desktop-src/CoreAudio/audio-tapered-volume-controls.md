---
description: Audio-Tapered controles de volume
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Audio-Tapered controles de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cca0879d27d0eba3d49ca22b019442f882bf917
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646384"
---
# <a name="audio-tapered-volume-controls"></a>Audio-Tapered controles de volume

A interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) gerencia os controles de volume que estão com um áudio cônico. Esses controles são adequados para aplicativos do Windows que exibem controles deslizantes de volume. Para um controle deslizante de volume que esteja vinculado a um controle de volume de áudio cônico, cada alteração na posição do controle deslizante produz uma alteração na intensidade percebida que é proporcional à distância percorrida pelo controle deslizante. Para uma distância de viagem específica, o valor pelo qual a intensidade percebida aumenta ou diminui é aproximadamente o mesmo, independentemente de a movimentação do controle deslizante ocorrer na parte inferior, superior ou intermediária do intervalo de movimento do controle deslizante. A intensidade percebida varia aproximadamente de forma linear com o logaritmo da potência do sinal de áudio.

O termo de *áudio cônico* originalmente referido à forma cônico do elemento resistive em um potentiometer que é usado como um controle de volume em um dispositivo de eletrônicos de áudio. Um elemento resistive cônico por áudio é mais largo na posição do volume zero e mais estreito na posição de volume máximo. O potentiometer controla o nível de tensão do sinal de áudio que o dispositivo desempenha por meio de seus alto-falantes. O cônico é projetado para produzir uma relação aproximadamente linear entre a posição do brisas potentiometer e a intensidade percebida nos alto-falantes. A relação entre a posição de brisas e a voltagem nos alto-falantes é não linear.

Por outro lado, um elemento resistive com um cônico linear tem uma largura uniforme sobre o intervalo de movimentação de potentiometer brisas. Como resultado, a tensão nos alto-falantes varia linearmente com a posição brisas. A relação entre a posição de brisas e a intensidade é não linear.

Da mesma forma, um aplicativo do Windows que exibe um controle deslizante de volume define uma relação entre a posição do slider e o nível de sinal de saída nos alto-falantes. A relação pode, na verdade, ser linear cônico ou um áudio cônico.

O diagrama a seguir mostra o mapeamento da posição do controle deslizante para a tensão de saída e para a intensidade percebida de um controle de volume cônico linear.

![diagrama de saída para um controle de volume cônico linear](images/taper1.jpg)

No lado esquerdo do diagrama anterior, o nível de tensão de saída do conversor de digital para analógico (DAC) de áudio aumenta linearmente conforme o controle deslizante de volume se move de sua posição mínima (rotulada como min) para sua posição máxima (rotulada como máxima). O rótulo V<sub>FS</sub> no eixo vertical representa a tensão de saída do DAC de escala total.

No entanto, a intensidade percebida varia aproximadamente como o logaritmo da potência do sinal de áudio, conforme mostrado no lado direito do diagrama anterior. Assim, a movimentação do controle deslizante sobre um intervalo próximo à configuração mínima resulta em uma alteração relativamente grande na intensidade percebida, mas a movimentação do controle deslizante sobre um intervalo da mesma largura perto da configuração máxima causa uma alteração relativamente pequena na intensidade percebida.

No lado direito do diagrama anterior, a intensidade no eixo vertical é medida em decibéis (dB) em relação à configuração de energia em escala total (em 0 decibéis). A curva de intensidade cruza o eixo vertical em menos infinito, mas apenas a parte da curva de 0 decibéis a – 96 decibéis aparece no diagrama. A decisão de mostrar apenas essa parte da curva é, de certa forma, arbitrária, mas – 96 decibéis convenientemente representa o poder no nível de saída próximo ao mais baixo de um DAC de 16 bits em relação ao poder de escala total. Esse valor é calculado como 20<sup>.</sup> log ₁ ₀ (1/65535).

Como pequenas alterações na posição do controle deslizante próximo à configuração mínima no diagrama anterior resultam em grandes alterações de intensidade, o usuário pode achar difícil controlar o volume nessa região. Movimentos de controle deslizante relativamente pequenos podem enviar por push o volume bem acima ou abaixo do nível desejado. Um controle de volume aprimorado forneceria uma relação mais linear entre a posição do controle deslizante e a intensidade.

O diagrama a seguir mostra o mapeamento da posição do controle deslizante para a tensão de saída e para a intensidade percebida de um controle de volume cônico por áudio.

![diagrama de saída para controle de volume cônico por áudio](images/taper2.jpg)

Conforme mostrado no lado direito do diagrama anterior, a intensidade percebida varia de forma linear com as alterações na posição do controle deslizante. Para que isso ocorra, a tensão DAC deve variar de forma não linear com a posição, conforme mostrado no lado esquerdo do diagrama. O assintoticamente de curva se aproxima de 0 volts à medida que o controle deslizante se move para a esquerda da configuração máxima. A tensão na posição do controle deslizante mínimo é muito pequena, mas pode não ser exatamente zero.

Os métodos a seguir na interface **IAudioEndpointVolume** usam configurações de volume que são medidas em decibéis:

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Esses métodos produzem uma relação aproximadamente linear entre a configuração de volume e a intensidade percebida. O intervalo de volumes em decibéis dos controles de volume que são gerenciados por esses métodos depende do dispositivo de ponto de extremidade de áudio. Para determinar o intervalo de volumes para um dispositivo específico, chame o método [**IAudioEndpointVolume:: GetVolumeRange**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange) .

Por outro lado, as configurações de volume para os métodos a seguir na interface **IAudioEndpointVolume** seguem uma curva mais gentilmente cônico no intervalo de volumes:

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

No Windows Vista, esses métodos usam uma curva intermediária entre a curva cônica de áudio mostrada no diagrama anterior e uma curva cônico linear. Observe que a forma da curva pode mudar em versões futuras do Windows. Os quatro primeiros métodos na lista anterior expressam os níveis de volume como valores normalizados no intervalo de 0,0 (volume mínimo) a 1,0 (volume máximo). Para os dois últimos métodos na lista, chame o método [**IAudioEndpointVolume:: GetVolumeStepInfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) para obter o número de etapas no intervalo de volumes.

As interfaces a seguir usam curvas com cônico linear para suas configurações de volume:

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Para obter mais informações sobre essas interfaces, consulte [controles de volume de sessão](session-volume-controls.md). E para obter informações sobre os intervalos de volume e os níveis de volume padrão nas várias versões do Windows, consulte [configurações de volume de áudio padrão](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles de volume](volume-controls.md)
</dt> </dl>

 

 
