---
description: As baterias podem fornecer energia para computadores portáteis e computadores em execução em uma fonte de alimentação ininterrupta (UPS).
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Informações da bateria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b1afd2461985ec85a07d40bd309c588a5404e4b59be7555a01fc6c147eb221
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143689"
---
# <a name="battery-information"></a>Informações da bateria

As baterias podem fornecer energia para computadores portáteis e computadores em execução em uma fonte de alimentação ininterrupta (UPS). Nesses computadores, o sistema operacional fornece informações sobre o estado da bateria para que os aplicativos possam fornecer funções úteis para o usuário. (Alguns sistemas de bateria não padrão mais antigos e UPSs não têm suporte.)

Observe que esta visão geral pressu que você está familiarizado com o gerenciamento [de dispositivos](/windows/desktop/DevIO/device-management).

Para obter informações sobre o status da bateria, use a [**função GetSystemPowerStatus,**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) que retorna informações gerais sobre todas as fontes de energia no sistema. Você deve usar **GetSystemPowerStatus** sempre que possível.

Em alguns casos, no entanto, são necessárias informações detalhadas sobre cada bateria individual. Para essa finalidade, cada dispositivo de bateria expõe uma interface IOCTL. As seguintes operações de IOCTL são executadas usando a [**função DeviceIoControl:**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

<dl>

[**INFORMAÇÕES DE CONSULTA DA BATERIA IOCTL \_ \_ \_**](ioctl-battery-query-information.md)  
[**STATUS DA CONSULTA DA BATERIA DE IOCTL \_ \_ \_**](ioctl-battery-query-status.md)  
[**MARCA DE \_ CONSULTA IOCTL BATTERY \_ \_**](ioctl-battery-query-tag.md)  
[**INFORMAÇÕES DO CONJUNTO DE BATERIA IOCTL \_ \_ \_**](ioctl-battery-set-information.md)  
</dl>

Para usar essa interface, um aplicativo deve seguir várias etapas. Primeiro, ele deve usar rotinas de instalação para enumerar todos os dispositivos que têm uma interface de classe de bateria. Observe que esses dispositivos representam as portas da bateria, não as baterias reais presentes no sistema. Em seguida, o aplicativo deve abrir um alça para cada dispositivo para que ele possa usar a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar solicitações para o dispositivo e, em seguida, adquirir marcas para as baterias inseridas. Depois de concluir essas etapas, o aplicativo pode enviar consultas para cada dispositivo de bateria.

## <a name="battery-tags"></a>Marcas de bateria

Como cada dispositivo de bateria representa um slot no qual uma bateria pode ser inserida, deve haver uma maneira de determinar quando a bateria é removida e reinserida, substituída ou alterada de qualquer outra maneira. Para fazer isso, cada bateria em um slot específico recebe uma marca. Essa marca deve ser usada para todas as consultas para obter informações. Se a marca fornecida pelo aplicativo não corresponder à bateria, a consulta falhará, indicando ao aplicativo que a bateria foi alterada de alguma forma. Para concluir a consulta com êxito, uma nova marca de bateria é necessária. Adquira a marca usando a [**operação \_ IOCTL BATTERY \_ QUERY \_ TAG.**](ioctl-battery-query-tag.md) Se uma bateria estiver presente nesse slot, a marca retornada poderá ser passada para qualquer uma das outras IOCTLs da bateria para executar outras funções. Em um sistema com várias bateria, cada dispositivo de bateria (slot) emite marcas de bateria independentemente, portanto, a marca de dois dispositivos separados às vezes pode ser idêntica.

Uma alteração na marca da bateria não significa necessariamente que a bateria foi removida e reinserada ou substituída. Uma nova marca poderá ser gerada se houver uma alteração em qualquer um dos dados que normalmente seriam estáticos. Por exemplo, quando uma bateria é carregada, a última capacidade totalmente carregada pode ter sido alterada. A marca também poderá mudar se a comunicação da bateria tiver sido perdida temporariamente ou se houver uma notificação incorreta do BIOS. Em alguns sistemas, a marca da bateria pode ser atualizada sempre que o status da AC é atualizado. Esse comportamento ocorre devido a uma característica do sistema de bateria e não é comum.

Sempre que a marca da bateria for atualizada, a bateria deverá ser tratada como se fosse uma nova bateria e todos os dados armazenados em cache devem ser lidos de novo. Se um aplicativo precisar saber se a mesma bateria física está presente, ele deverá verificar o valor de **BatteryUniqueID** no buffer de saída de [**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md) quando chamado com o nível de informações **BatteryUniqueID.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciamento de Energia](about-power-management.md)
</dt> <dt>

[Enumerando dispositivos de bateria](enumerating-battery-devices.md)
</dt> </dl>

 

 
