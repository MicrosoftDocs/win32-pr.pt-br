---
description: Exemplos de SDK que usam as APIs de áudio principais
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Exemplos de SDK que usam as APIs de áudio principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f875095579b40c6646d89e31328c148c5724c309
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479692"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Exemplos de SDK que usam as APIs de áudio principais

O Windows SDK inclui os exemplos de código a seguir que demonstram o uso das APIs de Áudio Principal. Os exemplos a seguir estão localizados no diretório %MSSdk% de áudio multimídia de exemplos, em que \\ \\ %MSSdk% é o diretório raiz da instalação do SDK do Windows em seu \\ computador.




| Amostra | Desascrição | 
|--------|--------------|
| <a href="aecmicarray.md">AECMicArray</a> | Este exemplo usa as APIs MMDevice, WASAPI, DeviceTopology e EndpointVolume para capturar um fluxo de voz de alta qualidade. O exemplo dá suporte ao AEC (cancelamento de eco acústico) e ao processamento de matriz de microfone usando o AEC DMO também chamado de DSP de captura de voz fornecido pela Microsoft. | 
| <a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a> | Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada, especificados pelo usuário e grava-os em um exclusivamente chamado . Arquivo WAV no diretório atual. Este exemplo demonstra o buffer orientado a eventos. | 
| <a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a> | Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada, especificados pelo usuário e grava-os em um exclusivamente chamado . Arquivo WAV no diretório atual. Este exemplo demonstra o buffer orientado por temporizador. | 
| <a href="duckingcapturesample.md">DuckingCaptureSample</a> | Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de rebaixamento que um aplicativo pode obter para implementar atenuação de fluxo. Esse aplicativo implementa um cliente de chat que usa APIs de áudio principais para ler dados de áudio de um dispositivo de comunicação e reproduzi-los no dispositivo de saída. | 
| <a href="endpointvolume.md">EndpointVolume</a> | Este aplicativo de exemplo usa as APIs de Áudio Principal para alterar o volume do dispositivo, especificado pelo usuário. | 
| <a href="osd.md">OSD</a> | Este exemplo usa as APIs MMDevice e EndpointVolume para implementar uma exibição na tela que mostra as alterações de volume no fluxo de saída que é reproduzido por meio do dispositivo de ponto de extremidade de renderização de áudio padrão. A exibição na tela é exibida quando o usuário ajusta o nível de volume no programa de controle de volume Windows, Sndvol.exe, e desaparece depois que o nível de volume permanece inalterado por um curto período. | 
| <a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a> | Este aplicativo de exemplo usa as APIs de Áudio Core para renderizar dados de áudio em um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer orientado a eventos para um cliente de renderização no modo exclusivo. Para um fluxo de modo exclusivo, o cliente compartilha o buffer do ponto de extremidade com o dispositivo de áudio. | 
| <a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a> | Este aplicativo de exemplo usa as APIs de Áudio Core para renderizar dados de áudio em um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer orientado por temporizador para um cliente de renderização no modo exclusivo. Para um fluxo de modo exclusivo, o cliente compartilha o buffer do ponto de extremidade com o dispositivo de áudio. | 
| <a href="rendersharedeventdriven.md">RenderSharedEventDriven</a> | Este aplicativo de exemplo usa as APIs de Áudio Core para renderizar dados de áudio em um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer orientado a eventos para um cliente de renderização no modo compartilhado. Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio. | 
| <a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a> | Este aplicativo de exemplo usa as APIs de Áudio Core para renderizar dados de áudio em um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer orientado por temporizador para um cliente de renderização no modo compartilhado. Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio. | 
| Winaudio | Este exemplo usa a API MMDevice e WASAPI para reproduzir e capturar fluxos de áudio. A interface do usuário deste aplicativo de exemplo permite que os usuários selecionem dispositivos de ponto de extremidade de áudio, alterem o nível de volume da sessão de áudio local e reproduzam arquivos .wav e entrada de microfone.<blockquote>[!Note]<br />Este exemplo foi preterido no Windows 7.</blockquote><br /> | 




 

Você pode baixar o Windows SDK do Microsoft Windows Site do Centro de [Download do SDK.](https://developer.microsoft.com/windows/downloads/sdk-archive/)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre as APIs Windows Core Audio](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




