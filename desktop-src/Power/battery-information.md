---
description: As baterias podem fornecer energia para computadores portáteis e computadores em execução em uma fonte de alimentação ininterrupta (UPS).
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Informações da bateria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766834"
---
# <a name="battery-information"></a>Informações da bateria

As baterias podem fornecer energia para computadores portáteis e computadores em execução em uma fonte de alimentação ininterrupta (UPS). Nesses computadores, o sistema operacional fornece informações sobre o estado da bateria para que os aplicativos possam fornecer funções úteis para o usuário. (Alguns sistemas de bateria não padrão mais antigos e UPSs não têm suporte.)

Observe que esta visão geral pressupõe que você esteja familiarizado com o [Gerenciamento de dispositivos](/windows/desktop/DevIO/device-management).

Para obter informações sobre o status da bateria, use a função [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) , que retorna informações gerais sobre todas as fontes de energia no sistema. Você deve usar **GetSystemPowerStatus** sempre que possível.

Em alguns casos, no entanto, são necessárias informações detalhadas sobre cada bateria individual. Para essa finalidade, cada dispositivo de bateria expõe uma interface de IOCTL. As seguintes operações de IOCTL são executadas usando a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) :

<dl>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)  
[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)  
[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)  
[**\_informações do \_ conjunto de baterias do IOCTL \_**](ioctl-battery-set-information.md)  
</dl>

Para usar essa interface, um aplicativo deve seguir várias etapas. Primeiro, ele deve usar rotinas de instalação para enumerar todos os dispositivos que têm uma interface de classe de bateria. Observe que esses dispositivos representam as portas de bateria, não as baterias reais presentes no sistema. O aplicativo deve, então, abrir um identificador para cada dispositivo para que ele possa usar a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar solicitações ao dispositivo e, em seguida, adquirir marcas para todas as baterias inseridas. Depois de concluir essas etapas, o aplicativo pode enviar consultas para cada dispositivo de bateria.

## <a name="battery-tags"></a>Marcas de bateria

Como cada dispositivo de bateria representa um slot no qual uma bateria pode ser inserida, deve haver uma maneira de determinar quando a bateria é removida e reinserida, substituída ou alterada de qualquer outra forma. Para fazer isso, é atribuída uma marca a cada bateria em um slot específico. Essa marca deve ser usada para todas as consultas para obter informações. Se a marca fornecida pelo aplicativo não corresponder à bateria, a consulta falhará, indicando ao aplicativo que a bateria mudou de alguma forma. Para concluir a consulta com êxito, uma nova marca de bateria é necessária. Adquira a marca usando a operação de [**\_ \_ \_ marca de consulta da bateria do IOCTL**](ioctl-battery-query-tag.md) . Se uma bateria estiver presente nesse slot, a marca retornada poderá ser passada para qualquer uma das outras IOCTLs de bateria para executar outras funções. Em um sistema com várias baterias, cada dispositivo de bateria (slot) emite marcas de bateria de forma independente, portanto, a marca de dois dispositivos separados pode, às vezes, ser idêntica.

Uma alteração na marca de bateria não significa necessariamente que a bateria foi removida e reinserida ou substituída. Uma nova marca pode ser gerada se houver uma alteração em qualquer um dos dados que normalmente seriam estáticos. Por exemplo, quando uma bateria é feita a cobrança, a última capacidade totalmente carregada pode ter mudado. A marca também pode mudar se a comunicação da bateria foi temporariamente perdida ou se houve uma notificação inadequada do BIOS. Em alguns sistemas, a marca de bateria pode ser atualizada sempre que o status de AC for alterado. Esse comportamento é devido a uma característica do sistema de bateria e não é comum.

Sempre que a marca de bateria é atualizada, a bateria deve ser tratada como se fosse uma nova bateria e todos os dados armazenados em cache devem ser lidos novamente. Se um aplicativo precisar saber se a mesma bateria física está presente, ele deve verificar o valor de **BatteryUniqueID** no buffer de saída das [**\_ \_ \_ informações de consulta da bateria do IOCTL**](ioctl-battery-query-information.md) quando chamado com o nível de informações **BatteryUniqueID** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> <dt>

[Enumerando dispositivos de bateria](enumerating-battery-devices.md)
</dt> </dl>

 

 
