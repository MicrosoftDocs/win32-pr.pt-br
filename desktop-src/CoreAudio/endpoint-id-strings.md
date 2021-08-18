---
description: Cadeias de caracteres de ID do ponto de extremidade
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Cadeias de caracteres de ID do ponto de extremidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fdfbf12f3e037a23163bb3e8fef525db89c15904328c9e0fd8a71e5de004b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957305"
---
# <a name="endpoint-id-strings"></a>Cadeias de caracteres de ID do ponto de extremidade

No Windows Vista, o sistema gera cadeias de caracteres de ID do ponto de extremidade para identificar os dispositivos de [ponto](audio-endpoint-devices.md) de extremidade de áudio no sistema. Uma cadeia de caracteres de ID do ponto de extremidade é uma cadeia de caracteres largos terminada em nulo. A cadeia de caracteres de ID do ponto de extremidade para um dispositivo de ponto de extremidade de áudio específico identifica exclusivamente o dispositivo entre todos os dispositivos de ponto de extremidade de áudio no sistema.

Se um sistema contiver dois ou mais dispositivos de adaptador de áudio idênticos, os dispositivos de ponto de extremidade de áudio correspondentes terão nomes amigáveis idênticos, mas cada dispositivo de ponto de extremidade terá uma cadeia de caracteres de ID de ponto de extremidade exclusiva. Para obter mais informações sobre como obter o nome amigável de um dispositivo de ponto de extremidade, consulte [Propriedades do dispositivo](device-properties.md).

Depois de obter uma instância de interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para um dispositivo de ponto de extremidade de áudio, um cliente pode chamar o método [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter a cadeia de caracteres de ID do ponto de extremidade para o dispositivo. Um cliente pode usar a cadeia de caracteres de ID do ponto de extremidade para criar uma instância do dispositivo de ponto de extremidade de áudio posteriormente ou em um processo diferente chamando o método [**IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)

Um cliente pode organizar para receber uma notificação quando o status de qualquer dispositivo de ponto de extremidade de áudio muda. Para receber notificações, o cliente implementa uma interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registra essa interface com a API MMDevice. Quando o status de um dispositivo de ponto de extremidade muda, a API MMDevice chama o método apropriado na interface [**EDataFlow do**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) cliente. Um dos parâmetros de entrada para o método é a cadeia de caracteres de ID do ponto de extremidade que identifica o dispositivo de ponto de extremidade cujo status foi alterado. Para obter mais informações sobre **o EDataFlow,** consulte [Eventos de dispositivo](device-events.md).

APIs de áudio herdadas, como DirectSound e as funções Windows multimídia, têm suas próprias interfaces para enumerar e identificar dispositivos de áudio. No Windows Vista, essas interfaces foram estendidas para fornecer as cadeias de caracteres de ID do ponto de extremidade que identificam os dispositivos de ponto de extremidade que baseam as abstrações de dispositivo apresentadas pelas APIs.

Durante a enumeração do dispositivo DirectSound, o DirectSound fornece a cadeia de caracteres de ID do ponto de extremidade para cada dispositivo enumerado. Para obter mais informações, consulte [Eventos de áudio para aplicativos de áudio herdado.](audio-events-for-legacy-audio-applications.md)

Para obter a cadeia de caracteres de ID do ponto de extremidade para um dispositivo waveform herdado, use a função [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) ou [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) para enviar uma mensagem DRV QUERYFUNCTIONINSTANCEID para o driver de dispositivo \_ waveform. Para ver um exemplo de código que mostra o uso dessa mensagem, consulte Funções de dispositivo para [aplicativos multimídia Windows herdados.](device-roles-for-legacy-windows-multimedia-applications.md)

Para obter mais informações sobre como usar as funcionalidades das PRINCIPAIS APIs de áudio para aprimorar aplicativos que usam APIs de áudio herdado, consulte Interoperabilidade com APIs de áudio [herdado](interoperability-with-legacy-audio-apis.md).

Os clientes devem tratar o conteúdo da cadeia de caracteres de ID do ponto de extremidade como opaco. Ou seja, os clientes não devem tentar analisar o conteúdo da cadeia de caracteres para obter informações sobre o dispositivo. O motivo é que o formato de cadeia de caracteres é indefinido e pode mudar de uma implementação do módulo do sistema de API MMDevice para a próxima.

O tempo de vida de uma cadeia de caracteres de ID do ponto de extremidade está vinculado à instalação do dispositivo. A cadeia de caracteres de ID do ponto de extremidade de um dispositivo será atualizada se o usuário atualizar o driver do dispositivo ou se o usuário desinstalar o dispositivo e instalá-lo novamente. No entanto, a cadeia de caracteres de ID do ponto de extremidade permanece inalterada entre as reinicializações do sistema e a cadeia de caracteres de ID do ponto de extremidade de um dispositivo de áudio USB permanecerá inalterada se o usuário desconectar o dispositivo e o conectar novamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> </dl>

 

 
