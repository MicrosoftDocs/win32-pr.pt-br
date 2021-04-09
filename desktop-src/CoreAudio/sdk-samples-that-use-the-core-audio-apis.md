---
description: Exemplos de SDK que usam as APIs de áudio principal
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Exemplos de SDK que usam as APIs de áudio principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920407"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Exemplos de SDK que usam as APIs de áudio principal

O SDK do Windows inclui os exemplos de código a seguir que demonstram o uso das APIs de áudio principais. Os exemplos a seguir estão localizados no diretório% MSSdk% \\ Sample \\ \\ áudio multimídia, em que% MSSdk% é o diretório raiz da instalação do SDK do Windows no seu computador.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Amostra</th>
<th>Deascription</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aecmicarray.md">AECMicArray</a></td>
<td>Este exemplo usa as APIs MMDevice, WASAPI, DeviceTopology e EndpointVolume para capturar um fluxo de voz de alta qualidade. O exemplo de Tnão dá suporte a um AEC (cancelamento de eco acústico) e ao processamento de matriz de microfone usando o AEC DMO também chamado de DSP de captura de voz fornecido pela Microsoft.</td>
</tr>
<tr class="even">
<td><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></td>
<td>Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada, especificado pelo usuário e grava-os em um nome exclusivo. Arquivo WAV no diretório atual. Este exemplo demonstra o buffer controlado por eventos.</td>
</tr>
<tr class="odd">
<td><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></td>
<td>Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada, especificado pelo usuário e grava-os em um nome exclusivo. Arquivo WAV no diretório atual. Este exemplo demonstra o buffer controlado por temporizador.</td>
</tr>
<tr class="even">
<td><a href="duckingcapturesample.md">DuckingCaptureSample</a></td>
<td>Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de pato que um aplicativo pode obter para implementar a atenuação de fluxo. Esse aplicativo implementa um cliente de chat que usa APIs de áudio de núcleo para ler dados de áudio de um dispositivo de comunicação e reproduzi-lo no dispositivo de saída.</td>
</tr>
<tr class="odd">
<td><a href="endpointvolume.md">EndpointVolume</a></td>
<td>Este aplicativo de exemplo usa as APIs de áudio principais para alterar o volume do dispositivo, especificado pelo usuário.</td>
</tr>
<tr class="even">
<td><a href="osd.md">OSD Feature</a></td>
<td>Este exemplo usa as APIs MMDevice e EndpointVolume para implementar uma exibição na tela que mostra as alterações de volume no fluxo de saída que é executado por meio do dispositivo de ponto de extremidade de renderização de áudio padrão. A exibição na tela é exibida quando o usuário ajusta o nível de volume no programa de controle de volume do Windows, Sndvol.exe e desaparece depois que o nível do volume permanece inalterado por um curto período de tempo.</td>
</tr>
<tr class="odd">
<td><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></td>
<td>Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer controlado por eventos para um cliente de renderização em modo exclusivo. Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.</td>
</tr>
<tr class="even">
<td><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></td>
<td>Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização em modo exclusivo. Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.</td>
</tr>
<tr class="odd">
<td><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></td>
<td>Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer controlado por eventos para um cliente de renderização no modo compartilhado. Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio.</td>
</tr>
<tr class="even">
<td><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></td>
<td>Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário. Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização no modo compartilhado. Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio.</td>
</tr>
<tr class="odd">
<td>WinAudio</td>
<td>Este exemplo usa a API MMDevice e o WASAPI para reproduzir e capturar fluxos de áudio. A interface do usuário deste aplicativo de exemplo permite que os usuários selecionem dispositivos de ponto de extremidade de áudio, alterem o nível de volume da sessão de áudio local e reproduza arquivos. wav e entrada de microfone.
<blockquote>
[!Note]<br />
Este exemplo foi preterido no Windows 7.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Você pode baixar o SDK do Windows no site do [centro de download do SDK do Microsoft Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre as APIs de áudio do Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




