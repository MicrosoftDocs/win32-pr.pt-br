---
description: Trabalhando com funções de dispositivo
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Trabalhando com funções de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7e3d0d2612415ddc3f72571774f11a2d62c911290b156be7efb543c48546e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406889"
---
# <a name="working-with-device-roles"></a>Trabalhando com funções de dispositivo

A [API MMDevice](mmdevice-api.md) dá suporte a funções de dispositivo. A enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) define as funções de dispositivo com suporte na API MMDevice.

> [!Note]  
> embora a [API MMDevice](mmdevice-api.md) dê suporte a funções de dispositivo, a interface do usuário no Windows Vista não implementa o suporte para esse recurso.

 

Um aplicativo pode usar a API MMDevice para dar suporte a [funções de dispositivo](device-roles.md) por meio dos métodos [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) e [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) . no entanto, a interface do usuário no Windows Vista não oferece suporte à atribuição de funções individuais a diferentes dispositivos. no Windows Vista, a interface do usuário permite que o usuário selecione um dispositivo de áudio padrão para renderização e um dispositivo de áudio padrão para captura. Quando o usuário seleciona um dispositivo de renderização ou de captura padrão, o sistema atribui todas as três funções de dispositivo (eConsole, eMultimedia e eCommunications) a esse dispositivo. Os aplicativos não podem alterar as funções atribuídas aos dispositivos de ponto de extremidade de áudio. O sistema operacional permite que apenas o usuário atribua funções de dispositivo.

Um cliente pode se registrar para receber uma notificação da API MMDevice sempre que uma alteração ocorrer na atribuição de funções para dispositivos de ponto de extremidade de áudio. Quando uma função muda de um dispositivo para outro, o cliente pode escolher se deseja continuar a reproduzir (ou gravar) seus fluxos por meio do mesmo dispositivo ou para alternar os fluxos para outro dispositivo. Por padrão, os fluxos continuam a ser reproduzidos (ou registrados) por meio do dispositivo original. no Windows Vista, para alternar os fluxos para outro dispositivo, o cliente deve excluir os fluxos no dispositivo original e criar fluxos de substituição no novo dispositivo. no Windows 7, o cliente pode escutar novas notificações para implementar um comutador contínuo sem interromper a reprodução ou a sessão de captura. Para obter mais informações, consulte [Roteamento de fluxo](stream-routing.md).

se você planeja usar o Windows Vista para testar seu aplicativo, você pode configurar um ambiente de teste para verificar se o aplicativo se comporta conforme o esperado quando o usuário pode atribuir funções de dispositivo individuais a diferentes dispositivos. Para obter mais informações, envie um email para uaa@microsoft.com.

## <a name="communication-devices"></a>Dispositivos de comunicação

a interface do usuário do Windows 7 tem a capacidade de adicionar *dispositivos de comunicação*. O painel de controle de **som** permite que o usuário selecione um dispositivo de comunicação padrão para renderizar e capturar o fluxo de áudio. Por padrão, quando um novo dispositivo está conectado ao computador, o sistema operacional executa a detecção automática de função e determina se o dispositivo é adequado para a função eCommunication. Ao direcionar dispositivos de comunicação, você pode desenvolver aplicativos que usam APIs de áudio de núcleo para implementar soluções de comunicação de PC-Phone. Por exemplo, um aplicativo VoIP pode atribuir seus fluxos de entrada e saída de voz para os dispositivos de ponto de extremidade de captura e renderização padrão com a função eCommunications. Como qualquer outro fluxo, um aplicativo de comunicação deve obter uma referência ao ponto de extremidade do dispositivo de comunicação chamando [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Nesta chamada, o aplicativo deve especificar **eCommunications** no parâmetro *role* . As operações de fluxo de WASAPI em um fluxo, abertas em um dispositivo de comunicação, são semelhantes a qualquer outro fluxo de áudio. O aplicativo de comunicação pode melhorar a experiência do usuário implementando comportamentos como o pato manipulando notificações do ponto de extremidade do dispositivo. Para obter mais informações, consulte [usando um dispositivo de comunicação](using-the-communication-device.md).

## <a name="automatic-device-role-detection"></a>Detecção automática de função de dispositivo

Considere um cenário no qual um computador tem um dispositivo de processamento padrão, os alto-falantes e um dispositivo de captura padrão, um microfone. O usuário conecta um headset USB ao computador. Depois que os drivers apropriados são instalados, o sistema operacional tenta detectar uma função a ser atribuída para o novo dispositivo de áudio.

no Windows 7, o recurso de detecção de função do dispositivo foi melhorado significativamente para determinar as funções apropriadas adequadas para dispositivos de áudio. Todos os dispositivos de áudio contêm um conjunto de definições de configuração preenchidas pelo OEM do dispositivo, que ajudam o sistema a decidir como usar o dispositivo. Essas configurações incluem informações como o local físico da tomada de áudio do tipo de dispositivo, o subtipo da tomada e os recursos de detecção para que o sistema possa determinar se o dispositivo está conectado. Ao recuperar esses valores do dispositivo, o sistema operacional determina a função a ser atribuída ao dispositivo. Nesse cenário, o sistema consultou o dispositivo headset USB, executou a detecção automática de função e decidiu que o dispositivo é mais adequado para ser um dispositivo de comunicação.

Um aplicativo também pode obter informações sobre a tomada usando as APIs de áudio principais. Para obter mais informações, consulte [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) e [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de dispositivo](device-roles.md)
</dt> </dl>

 

 



