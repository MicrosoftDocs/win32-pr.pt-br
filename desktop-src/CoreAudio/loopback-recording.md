---
description: Gravação de loopback
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Gravação de loopback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa5ffe48bf11ad57b02085ab00dfd1ca09be0f72a56935cbd8d1bb40543033f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005269"
---
# <a name="loopback-recording"></a>Gravação de loopback

No modo de loopback, um cliente de WASAPI pode capturar o fluxo de áudio que está sendo interpretado por um dispositivo de ponto de extremidade de renderização. Para abrir um fluxo no modo de loopback, o cliente deve:

-   Obtenha uma [**interface IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para o dispositivo de ponto de extremidade de renderização.
-   Inicialize um fluxo de captura no modo de loopback no dispositivo de ponto de extremidade de renderização.

Depois de seguir essas etapas, o cliente pode chamar o método [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obter uma interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) no dispositivo de ponto de extremidade de renderização.

WASAPI fornece o modo de loopback principalmente para dar suporte ao cancelamento de eco acústico (AEC). No entanto, outros tipos de aplicativos de áudio podem achar o modo de loopback útil para capturar a combinação de sistema que está sendo tocada pelo mecanismo de áudio.

No exemplo de código em [Capturando um Fluxo](capturing-a-stream.md), a função RecordAudioStream pode ser facilmente modificada para configurar um fluxo de captura de modo loopback. As modificações necessárias são:

-   Na chamada para o método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint,**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) altere o primeiro parâmetro (*dataFlow*) de eCapture para eRender.
-   Na chamada para o método [**IAudioClient::Initialize,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) altere o valor do segundo parâmetro (*StreamFlags*) de 0 para AUDCLNT \_ STREAMFLAGS \_ LOOPBACK.

Em versões do Windows anteriores ao Windows 10 1703, o cliente de captura de modo de pull não recebe nenhum evento quando um fluxo é inicializado com buffer orientado a eventos e está habilitado para loopback. Para resolver isso, inicialize um fluxo de renderização no modo orientado a eventos. Sempre que o cliente recebe um evento para o fluxo de renderização, ele deve sinalizar ao cliente de captura para executar o thread de captura que lê o próximo conjunto de exemplos do buffer do ponto de extremidade de captura. Nas Windows 10 1703 e superiores, os clientes de loopback orientados a eventos têm suporte e não precisam mais da solução alternativa que envolve o fluxo de renderização.  

Um cliente pode habilitar o modo de loopback somente para um fluxo de modo compartilhado (AUDCLNT \_ SHAREMODE \_ SHARED). Os fluxos de modo exclusivo não podem operar no modo de loopback.

A implementação de loopback por WASAPI depende dos recursos do hardware. Se o hardware dá suporte a um pino de loopback no ponto de extremidade de renderização, o WASAPI usa o áudio fornecido nesse pino para o fluxo de loopback. Quando o hardware não dá suporte a um pino de loopback, o WASAPI copia o fluxo de saída do mecanismo de áudio para o buffer de captura do aplicativo de loopback, além de copiar os dados de áudio para o pino de renderização do hardware.

Alguns fornecedores de hardware implementam dispositivos de loopback (em vez de fixar instâncias em dispositivos de renderização) em seus adaptadores de áudio. Embora os dispositivos de loopback de hardware sejam semelhantes em operação ao modo de loopback WASAPI, eles podem ser mais difíceis de usar.

Os dispositivos de loopback de hardware têm as seguintes desvantagens para aplicativos de áudio:

-   Nem todos os adaptadores de áudio têm dispositivos de loopback. Portanto, os aplicativos que dependem deles não funcionarão em todos os sistemas.
-   Antes que um aplicativo possa registrar de um dispositivo de loopback, o usuário deve identificar o dispositivo de loopback e habilita-lo para uso.

Fornecedores diferentes atribuem nomes diferentes aos seus dispositivos de loopback de hardware. Os seguintes nomes são exemplos:

-   Combinação estéreo
-   Waveout Mix
-   Saída misturada
-   O que você ouvir

A falta de nomes padronizados pode fazer com que os usuários tenham dificuldade para identificar um dispositivo de loopback em uma lista de nomes de dispositivo.

Um dispositivo de loopback de hardware é um dispositivo de captura. Portanto, se um adaptador dá suporte a um dispositivo de loopback, um aplicativo de áudio pode gravar do dispositivo da mesma maneira que registra de qualquer outro dispositivo de captura.

Por exemplo, se você selecionar um dispositivo de loopback de hardware para ser o dispositivo de captura padrão, poderá usar [a](capturing-a-stream.md) função RecordAudioStream (sem modificação) no exemplo de código em Capturando um fluxo para capturar o fluxo do dispositivo. (Você também pode usar uma API de áudio herdada, como as funções **Windows waveInXxx** multimídia, para capturar o fluxo do dispositivo.)

Se o adaptador de áudio contiver um dispositivo de loopback de hardware, você poderá usar o painel de controle Windows multimídia, Mmsys.cpl, para designar o dispositivo como o dispositivo de captura padrão. As etapas são as seguintes:

1.  Para executar Mmsys.cpl, abra uma janela do Prompt de Comando e insira o seguinte comando:

    ```C++
    control mmsys.cpl,,1
    ```

    

    Como alternativa, você pode executar Mmsys.cpl clicando com o botão direito do mouse no ícone do locutor na área de notificação, que está localizada no lado direito da barra de tarefas e selecionando Gravando **Dispositivos**.

2.  Depois que a Mmsys.cpl janela for aberta, clique com o botão direito do mouse em qualquer lugar na lista de dispositivos de gravação e verifique se a opção Mostrar Dispositivos **Desabilitados** está marcada. (Caso contrário, se o dispositivo de loopback estiver desabilitado, ele não aparecerá na lista.)
3.  Procure a lista de dispositivos de gravação para localizar o dispositivo de loopback (se ele existir). Se o dispositivo de loopback estiver desabilitado, habilita-o clicando com o botão direito do mouse no dispositivo e clicando em **Habilitar**.
4.  Por fim, para selecionar o dispositivo de loopback para ser o dispositivo de captura padrão, clique com o botão direito do mouse no dispositivo e clique em **Definir como Dispositivo Padrão.**

WASAPI dá suporte à gravação de loopback, independentemente de o hardware de áudio conter um dispositivo de loopback ou se o usuário habilitar o dispositivo.

Windows O Vista fornece DRM (gerenciamento de direitos digitais). Os provedores de conteúdo dependem do DRM para proteger suas músicas proprietárias ou outros conteúdos contra cópia não autorizada e outros usos ilícitos. Da mesma forma, um driver de áudio confiável não permite que um dispositivo de loopback capture fluxos digitais que contenham conteúdo protegido. Windows O Vista permite que apenas drivers confiáveis reproduzam conteúdo protegido. Para obter mais informações sobre drivers confiáveis e DRM, consulte a documentação Windows DDK.

O loopback WASAPI contém a combinação de todo o áudio que está sendo tocado, independentemente da sessão dos Serviços de Terminal da qual o áudio foi originado. Por exemplo, você pode executar um cliente de loopback em um serviço em execução na sessão 0 e capturar áudio de todas as sessões de usuário, bem como o áudio sendo executado da sessão 0.

Área de Trabalho Remota permite redirecionar áudio para o cliente. Isso é implementado criando novos dispositivos de áudio que aparecem apenas para essa sessão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Fluxo](stream-management.md)
</dt> </dl>

 

 



