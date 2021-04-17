---
description: Cadeias de ID do ponto de extremidade
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Cadeias de ID do ponto de extremidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04c07da78b92795ebadd7d8f9731f7188ae8dc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749298"
---
# <a name="endpoint-id-strings"></a>Cadeias de ID do ponto de extremidade

No Windows Vista, o sistema gera cadeias de caracteres de ID de ponto de extremidade para identificar os [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema. Uma cadeia de caracteres de ID de ponto de extremidade é uma cadeia de caracteres largo com terminação nula. A cadeia de caracteres de ID do ponto de extremidade para um dispositivo de ponto de extremidade de áudio específico identifica exclusivamente o dispositivo entre todos os dispositivos de ponto de extremidade de áudio no sistema

Se um sistema tiver dois ou mais dispositivos de adaptador de áudio idênticos, os dispositivos de ponto de extremidade de áudio correspondentes terão nomes amigáveis idênticos, mas cada dispositivo de ponto de extremidade terá uma cadeia de caracteres de ID de ponto de extremidade exclusiva Para obter mais informações sobre como obter o nome amigável de um dispositivo de ponto de extremidade, consulte [Propriedades do dispositivo](device-properties.md).

Depois de obter uma instância de interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para um dispositivo de ponto de extremidade de áudio, um cliente pode chamar o método [**IMMDevice:: GetID**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter a cadeia de caracteres de ID do ponto de extremidade para o dispositivo. Um cliente pode usar a cadeia de caracteres de ID do ponto de extremidade para criar uma instância do dispositivo de ponto de extremidade de áudio em um momento posterior ou em um processo diferente chamando o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .

Um cliente pode se organizar para receber uma notificação quando o status de qualquer dispositivo de ponto de extremidade de áudio for alterado. Para receber notificações, o cliente implementa uma interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registra essa interface com a API MMDevice. Quando o status de um dispositivo de ponto de extremidade é alterado, a API MMDevice chama o método apropriado na interface [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) do cliente. Um dos parâmetros de entrada para o método é a cadeia de caracteres de ID do ponto de extremidade que identifica o dispositivo de ponto de extremidade cujo status foi alterado. Para obter mais informações sobre **EDataFlow**, consulte [eventos de dispositivo](device-events.md).

As APIs de áudio herdadas, como DirectSound e as funções de multimídia do Windows, têm suas próprias interfaces para enumerar e identificar dispositivos de áudio. No Windows Vista, essas interfaces foram estendidas para fornecer as cadeias de caracteres de ID de ponto de extremidade que identificam os dispositivos de ponto de extremidade que se desdão às abstrações de dispositivo apresentadas pelas APIs.

Durante a enumeração do dispositivo DirectSound, o DirectSound fornece a cadeia de caracteres de ID do ponto de extremidade para cada dispositivo enumerado. Para obter mais informações, consulte [eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md).

Para obter a cadeia de caracteres de ID de ponto de extremidade para um dispositivo de forma de onda herdado, use a função [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) ou [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) para enviar uma \_ mensagem QUERYFUNCTIONINSTANCEID drv para o driver de dispositivo de forma de onda. Para obter um exemplo de código que mostra o uso dessa mensagem, consulte [funções de dispositivo para aplicativos multimídia herdados do Windows](device-roles-for-legacy-windows-multimedia-applications.md).

Para obter mais informações sobre como usar os recursos das APIs de áudio principal para aprimorar aplicativos que usam APIs de áudio herdadas, consulte [interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md).

Os clientes devem tratar o conteúdo da cadeia de caracteres de ID do ponto de extremidade como opaco. Ou seja, os clientes não devem tentar analisar o conteúdo da cadeia de caracteres para obter informações sobre o dispositivo. O motivo é que o formato da cadeia de caracteres é indefinido e pode ser alterado de uma implementação do módulo sistema da API MMDevice para o próximo.

O tempo de vida de uma cadeia de caracteres de ID de ponto de extremidade é vinculado à instalação do dispositivo. A cadeia de caracteres de ID de ponto de extremidade de um dispositivo será alterada se o usuário atualizar o driver de dispositivo ou se o usuário desinstalar o dispositivo e o instalar novamente. No entanto, a cadeia de caracteres de ID de ponto de extremidade permanece inalterada entre as reinicializações do sistema e a cadeia de caracteres de ID do ponto de extremidade de um dispositivo de áudio USB permanece inalterada se o usuário desconectar o dispositivo e o conectar novamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> </dl>

 

 
