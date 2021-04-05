---
description: No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio de núcleo como Media Foundation, DirectSound e APIs Wave, implementam o recurso de roteamento de fluxo manipulando a alternância de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obtendo o ponto de extremidade do dispositivo para roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826433"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Obtendo o ponto de extremidade do dispositivo para roteamento de fluxo

No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio de núcleo como Media Foundation, DirectSound e APIs Wave, implementam o recurso de roteamento de fluxo manipulando a alternância de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão. Aplicativos de mídia que usam essas APIs (por exemplo, um aplicativo ativando um objeto **IDirectSound** ou **IBaseFilter** em um objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) usam o comportamento de roteamento de fluxo sem nenhuma modificação na origem.

As APIs de alto nível implementam o roteamento de fluxo para o ponto de extremidade do dispositivo que é obtido por meio de [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Se um aplicativo transmitir para o dispositivo padrão, o recurso de roteamento de fluxo funcionará conforme definido. Os fluxos não serão alternados para o novo dispositivo se ele for recuperado por qualquer outro mecanismo, mesmo se for o mesmo que o dispositivo padrão.

Um aplicativo de mídia que usa APIs de áudio de núcleo diretamente (cliente WASAPI) pode fornecer uma implementação de roteamento de fluxo personalizada para qualquer dispositivo de renderização ou de captura. Um cliente WASAPI pode replicar o implemetation fornecido pelas APIs de alto nível restringindo-o a fluxos que são abertos em dispositivos que são definidos como o dispositivo padrão. Para obter uma referência ao ponto de extremidade do dispositivo padrão, o cliente deve chamar [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Nesta chamada, o cliente deve indicar se ele requer um ponteiro para o dispositivo padrão de renderização ou o dispositivo padrão de captura especificando o parâmetro *Dataflow* . O cliente também deve especificar a função apropriada para o ponto de extremidade no atributo **ERole** (**eConsole** ou **eCommunications**). Não use **eMultimedia**.

Se o aplicativo flui para qualquer outro dispositivo, o aplicativo pode obter o dispositivo especificando uma cadeia de caracteres de ID de ponto de extremidade (chamando [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Depois que o dispositivo é identificado, o cliente WASAPI pode fornecer a implementação para o roteamento de fluxo manipulando as notificações de sessão de dispositivo e de áudio enviadas para o dispositivo. Para obter mais informações sobre essas notificações, consulte [notificações relevantes para o roteamento de fluxo](relevant-device-notifications-for-stream-routing.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API do MMDevice](mmdevice-api.md)
</dt> <dt>

[Sobre o WASAPI](wasapi.md)
</dt> <dt>

[Roteamento de fluxo](stream-routing.md)
</dt> </dl>

 

 



