---
description: Funções de dispositivo
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Funções de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089247"
---
# <a name="device-roles"></a>Funções de dispositivo

Se um sistema contiver dois ou mais dispositivos de ponto de extremidade de renderização de áudio, um dispositivo poderá ser melhor para a execução de um tipo de conteúdo de áudio, e outro dispositivo poderá ser melhor para reproduzir outro tipo de conteúdo. Por exemplo, se um sistema tiver dois dispositivos de renderização, o usuário poderá optar por reproduzir música em um dispositivo e reproduzir sons de notificação do sistema no outro.

Da mesma forma, se um sistema contiver dois ou mais dispositivos de ponto de extremidade de captura de áudio, um dispositivo poderá ser melhor para capturar um tipo de conteúdo de áudio e outro dispositivo poderá ser melhor para capturar outro tipo de conteúdo. Por exemplo, se um sistema tiver dois dispositivos de captura, o usuário poderá optar por gravar música ao vivo em um dispositivo e usar o outro dispositivo para comandos de voz.

Os dispositivos podem ter três funções: console, comunicações e multimídia. a tabela a seguir descreve as funções de dispositivo identificadas pelas três constantes — eConsole, eCommunications e eMultimedia — na enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .



| Constante ERole  | Função do dispositivo                              | Exemplos de renderização             | Exemplos de captura                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| eConsole        | Interação com o computador            | Jogos e notificações do sistema | Comandos de voz                     |
| eCommunications | Comunicações de voz com outra pessoa | Bate-papo e VoIP                  | Bate-papo e VoIP                      |
| eMultimedia     | Reprodução ou gravação de conteúdo de áudio       | Música e filmes               | Narração e gravação de música ao vivo |



 

Um dispositivo de renderização ou de captura específico pode ser atribuído a nenhuma, uma, algumas ou todas as funções na tabela anterior. A qualquer momento, cada função na tabela é atribuída a um dispositivo de renderização (e apenas um) e a um (e apenas um) dispositivo de captura. Ou seja, a atribuição de funções para processar dispositivos é independente da atribuição de funções para capturar dispositivos.

Um aplicativo pode optar por reproduzir todos os seus fluxos de saída por meio de um único dispositivo de ponto de extremidade de renderização e registrar todos os seus fluxos de entrada de um único dispositivo de ponto de extremidade de captura. Como alternativa, um aplicativo pode optar por reproduzir alguns dos fluxos de saída por meio de um dispositivo de renderização e reproduzir outros fluxos de saída por meio de outro dispositivo de renderização. Da mesma forma, ele pode optar por registrar alguns de seus fluxos de entrada por meio de um dispositivo de captura e registrar outros fluxos de entrada por meio de outro dispositivo de captura. Em todos os casos, o aplicativo pode atribuir cada fluxo ao dispositivo cuja função é mais apropriada para esse fluxo.

Por exemplo, um aplicativo VoIP pode atribuir o fluxo de saída que contém a notificação de toque para o dispositivo de ponto de extremidade de renderização com a função eConsole.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> <dt>

[Trabalhando com funções de dispositivo](device-roles-in-windows-vista.md)
</dt> <dt>

[Interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



