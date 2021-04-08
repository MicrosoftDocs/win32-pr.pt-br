---
description: Gravação de loopback
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Gravação de loopback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374da7497096118905f5e4c79bbacda832a42a7b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920485"
---
# <a name="loopback-recording"></a>Gravação de loopback

No modo de loopback, um cliente do WASAPI pode capturar o fluxo de áudio que está sendo reproduzido por um dispositivo de ponto de extremidade de renderização. Para abrir um fluxo no modo de loopback, o cliente deve:

-   Obtenha uma interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para o dispositivo de ponto de extremidade de renderização.
-   Inicializar um fluxo de captura no modo de loopback no dispositivo de ponto de extremidade de renderização.

Depois de seguir essas etapas, o cliente pode chamar o método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obter uma interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) no dispositivo de ponto de extremidade de renderização.

O WASAPI fornece o modo de auto-retorno principalmente para dar suporte a cancelamento de eco acústico (AEC). No entanto, outros tipos de aplicativos de áudio podem encontrar o modo de loopback útil para capturar a combinação do sistema que está sendo reproduzida pelo mecanismo de áudio.

No exemplo de código na [captura de um fluxo](capturing-a-stream.md), a função RecordAudioStream pode ser facilmente modificada para configurar um fluxo de captura de modo de loopback. As modificações necessárias são:

-   Na chamada para o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , altere o primeiro parâmetro (*Dataflow*) de eCapture para eRender.
-   Na chamada para o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , altere o valor do segundo parâmetro (*StreamFlags*) de 0 para AUDCLNT \_ StreamFlags \_ loopback.

Em versões do Windows anteriores ao Windows 10 1703, o cliente de captura de modo de pull não recebe nenhum evento quando um fluxo é inicializado com buffer controlado por eventos e é habilitado para loopback. Para contornar isso, inicialize um fluxo de renderização no modo orientado a eventos. Cada vez que o cliente recebe um evento para o fluxo de renderização, ele deve sinalizar o cliente de captura para executar o thread de captura que lê o próximo conjunto de amostras do buffer de ponto de extremidade de captura. No Windows 10 versões 1703 e superiores, os clientes de loopback orientados por eventos têm suporte e não precisam mais da solução que envolve o fluxo de renderização.  

Um cliente pode habilitar o modo de loopback somente para um fluxo de modo compartilhado (AUDCLNT \_ ShareMode \_ compartilhado). Os fluxos de modo exclusivo não podem operar no modo de loopback.

A implementação de auto-retorno por WASAPI depende dos recursos do hardware. Se o hardware der suporte a um PIN de loopback no ponto de extremidade de renderização, o WASAPI usará o áudio fornecido nesse PIN para o fluxo de loopback. Quando o hardware não dá suporte a um PIN de loopback, o WASAPI copia o fluxo de saída do mecanismo de áudio para o buffer de captura do aplicativo de loopback, além de copiar os dados de áudio para o PIN de renderização do hardware.

Alguns fornecedores de hardware implementam dispositivos de auto-retorno (em vez de fixar instâncias em dispositivos de processamento) em seus adaptadores de áudio. Embora os dispositivos de loopback de hardware sejam semelhantes em operação ao modo de loopback WASAPI, eles podem ser mais difíceis de usar.

Os dispositivos de loopback de hardware têm as seguintes desvantagens para aplicativos de áudio:

-   Nem todos os adaptadores de áudio têm dispositivos de loopback. Assim, os aplicativos que dependem deles não funcionarão em todos os sistemas.
-   Antes que um aplicativo possa ser gravado de um dispositivo de loopback, o usuário deve identificar o dispositivo de loopback e habilitá-lo para uso.

Fornecedores diferentes atribuem nomes diferentes aos seus dispositivos de loopback de hardware. Os seguintes nomes são exemplos:

-   Mixagem estéreo
-   Mixagem de WaveOut
-   Saída mista
-   O que você ouve

A falta de nomes padronizados pode fazer com que os usuários tenham dificuldade para identificar um dispositivo de loopback em uma lista de nomes de dispositivos.

Um dispositivo de loopback de hardware é um dispositivo de captura. Portanto, se um adaptador oferecer suporte a um dispositivo de loopback, um aplicativo de áudio poderá gravar do dispositivo da mesma maneira que ele registra de qualquer outro dispositivo de captura.

Por exemplo, se você selecionar um dispositivo de loopback de hardware para ser o dispositivo de captura padrão, poderá usar a função RecordAudioStream (sem modificação) no exemplo de código na [captura de um fluxo](capturing-a-stream.md) para capturar o fluxo do dispositivo. (Você também pode usar uma API de áudio herdada, como as funções de **waveInXxx** de multimídia do Windows, para capturar o fluxo do dispositivo.)

Se o adaptador de áudio contiver um dispositivo de loopback de hardware, você poderá usar o painel de controle multimídia do Windows, Mmsys.cpl, para designar o dispositivo como o dispositivo de captura padrão. As etapas são as seguintes:

1.  Para executar Mmsys.cpl, abra uma janela de prompt de comando e digite o seguinte comando:

    ```C++
    control mmsys.cpl,,1
    ```

    

    Como alternativa, você pode executar Mmsys.cpl clicando com o botão direito do mouse no ícone de alto-falante na área de notificação, que está localizada no lado direito da barra de tarefas e selecionando **dispositivos de gravação**.

2.  Depois que a janela de Mmsys.cpl for aberta, clique com o botão direito do mouse em qualquer lugar da lista de dispositivos de gravação e verifique se a opção **Mostrar dispositivos desabilitados** está marcada. (Caso contrário, se o dispositivo de loopback estiver desabilitado, ele não será exibido na lista.)
3.  Procure a lista de dispositivos de gravação para localizar o dispositivo de loopback (se existir). Se o dispositivo de loopback estiver desabilitado, habilite-o clicando com o botão direito do mouse no dispositivo e clicando em **habilitar**.
4.  Por fim, para selecionar o dispositivo de loopback para ser o dispositivo de captura padrão, clique com o botão direito do mouse no dispositivo e clique em **definir como dispositivo padrão**.

O WASAPI dá suporte à gravação de auto-retorno, independentemente de o hardware de áudio conter um dispositivo de loopback ou se o usuário habilitou o dispositivo.

O Windows Vista fornece DRM (gerenciamento de direitos digitais). Os provedores de conteúdo dependem do DRM para proteger suas músicas proprietárias ou outros conteúdos de cópias não autorizadas e outros usos inválidos. Da mesma forma, um driver de áudio confiável não permite que um dispositivo de loopback Capture fluxos digitais que contêm conteúdo protegido. O Windows Vista permite que apenas drivers confiáveis reproduzam conteúdo protegido. Para obter mais informações sobre drivers confiáveis e DRM, consulte a documentação do Windows DDK.

O loopback WASAPI contém a combinação de todos os áudios que estão sendo reproduzidos, independentemente da sessão dos serviços de terminal da qual o áudio foi originado. Por exemplo, você pode executar um cliente de auto-retorno em um serviço em execução na sessão 0 e capturar áudio de todas as sessões de usuário, bem como o áudio que está sendo reproduzido da sessão 0.

Área de Trabalho Remota permite redirecionar o áudio para o cliente. Isso é implementado pela criação de novos dispositivos de áudio que aparecem apenas para essa sessão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de fluxo](stream-management.md)
</dt> </dl>

 

 



