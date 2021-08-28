---
description: No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio principais, como Media Foundation, DirectSound e WAVE APIs, implementam o recurso de roteamento de fluxo manipulando a troca de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obter o ponto de extremidade do dispositivo para roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb45560bc8a27e4641e5d52c8fed0bee51c877dbec4d098bb5232830359f0b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695386"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Obter o ponto de extremidade do dispositivo para roteamento de fluxo

No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio principais, como Media Foundation, DirectSound e WAVE APIs, implementam o recurso de roteamento de fluxo manipulando a troca de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão. Os aplicativos de mídia que usam essas APIs (por exemplo, um aplicativo que ativa um objeto **IDirectSound** ou **IBaseFilter** em um objeto [**IMMDevice)**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) usam o comportamento de roteamento de fluxo sem nenhuma modificação na origem.

As APIs de alto nível implementam o roteamento de fluxo para o ponto de extremidade do dispositivo obtido por meio [**de IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Se um aplicativo transmitir para o dispositivo padrão, o recurso de roteamento de fluxo funcionará conforme definido. Fluxos serão alternados para o novo dispositivo se ele for recuperado por qualquer outro mecanismo, mesmo que ele seja o mesmo que o dispositivo padrão.

Um aplicativo de mídia que usa APIs de áudio principais diretamente (cliente WASAPI) pode fornecer uma implementação de roteamento de fluxo personalizada para qualquer dispositivo de renderização ou captura. Um cliente WASAPI pode replicar a implemetação fornecida pelas APIs de alto nível restringindo-a a fluxos abertos em dispositivos definidos como o dispositivo padrão. Para obter uma referência ao ponto de extremidade do dispositivo padrão, o cliente deve chamar [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Nessa chamada, o cliente deve indicar se ele requer um ponteiro para o dispositivo padrão de renderização ou o dispositivo padrão de captura especificando o *parâmetro dataFlow.* O cliente também deve especificar a função apropriada para o ponto de extremidade no atributo **ERole** (**eConsole** ou **eCommunications**). Não use **eMultimedia**.

Se o aplicativo transmitir para qualquer outro dispositivo, o aplicativo poderá obter o dispositivo especificando uma cadeia de caracteres de ID do ponto de extremidade (chamando [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Depois que o dispositivo é identificado, o cliente WASAPI pode fornecer a implementação para roteamento de fluxo manipulando as notificações de sessão de áudio e dispositivo enviadas para o dispositivo. Para obter mais informações sobre essas notificações, consulte [Notificações relevantes para roteamento de fluxo.](relevant-device-notifications-for-stream-routing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API MMDevice](mmdevice-api.md)
</dt> <dt>

[Sobre WASAPI](wasapi.md)
</dt> <dt>

[Roteamento de fluxo](stream-routing.md)
</dt> </dl>

 

 



