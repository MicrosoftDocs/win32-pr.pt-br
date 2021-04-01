---
title: Registrando um dispositivo hospedado no host do dispositivo
description: Registrar um dispositivo hospedado significa fornecer o host do dispositivo com a descrição do dispositivo e seu objeto de controle de dispositivo.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a607af4f6ada359a9ee32e98e416d8271fd502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159735"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Registrando um dispositivo hospedado no host do dispositivo

Registrar um dispositivo hospedado significa fornecer o host do dispositivo com a descrição do dispositivo e seu objeto de controle de dispositivo. Em seguida, o host do dispositivo constrói uma descrição completa do dispositivo UPnP, publica-o e anuncia o dispositivo na rede usando o protocolo de descoberta UPnP. Depois que um dispositivo for publicado, ele estará disponível para pontos de controle.

Os dispositivos são registrados de duas maneiras:

-   Um aplicativo cria uma instância do objeto de controle de dispositivo e passa um ponteiro para ele para o host do dispositivo.
-   O aplicativo passa o ProgID de um objeto de controle de dispositivo registrado para o host do dispositivo. O host do dispositivo instancia-o quando o host do dispositivo recebe a primeira solicitação para o dispositivo.

Independentemente de qual método é usado, o host do dispositivo publica e anuncia o dispositivo assim que ele é registrado. A diferença entre as duas abordagens tem a ver com quando o código do dispositivo é carregado. Quando o aplicativo passa um ponteiro para o objeto de controle de dispositivo, o código do dispositivo é carregado e em execução no momento do registro. Quando o aplicativo passa um ProgID, o código do dispositivo só é carregado quando uma ação é chamada, uma propriedade é consultada ou uma solicitação de assinatura de evento chega. A segunda abordagem é um pouco mais eficiente. No entanto, ele não é adequado para dispositivos que devem estar em execução antes que todas as solicitações de assinatura de evento ou controle cheguem, porque usar essa abordagem, os objetos de controle de dispositivo são criados apenas quando são necessários. Esse segundo método também pode criar problemas de desempenho ao receber a primeira solicitação para um tipo de dispositivo.

Se você quiser garantir que um dispositivo seja anunciado automaticamente pelo host do dispositivo na rede quando o computador for iniciado, invoque [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice). O **RegisterDevice** garante que o código do dispositivo seja carregado apenas quando uma solicitação de assinatura de evento ou controle for recebida.

Se seus dispositivos forem transitórios ou ligados, invoque [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)e o dispositivo não será automaticamente anunciado quando o computador for reiniciado.

## <a name="discovery-announcement-lifetime"></a>Tempo de vida do anúncio de descoberta

Cada dispositivo registrado com o host do dispositivo é associado a um tempo de vida, que é especificado pelo dispositivo após o registro. O tempo de vida do dispositivo é o período durante o qual os comunicados de descoberta do dispositivo são válidos. O tempo de vida é passado para o ponto de controle como um cabeçalho no anúncio de descoberta inicial. O host do dispositivo atualiza automaticamente o comunicado antes do tempo de expiração. Os valores do tempo de vida do anúncio de descoberta devem ser 15 minutos ou mais (o padrão é 30 minutos).

## <a name="device-identifiers-created-at-registration"></a>Identificadores de dispositivo criados no registro

Ao criar um modelo de descrição do dispositivo, o desenvolvedor do dispositivo deve fornecer o caminho do recurso para a descrição do serviço e os ícones associados. O caminho do recurso é determinado pelo aplicativo do dispositivo.

Como o mesmo dispositivo pode ser registrado várias vezes no mesmo computador, o UDN especificado no modelo de descrição do dispositivo não é suficiente para identificar exclusivamente um dispositivo. Portanto, quando um dispositivo é registrado, o host do dispositivo cria um identificador de dispositivo. Esse identificador de dispositivo, em associação com o UDN no modelo de descrição do dispositivo, pode ser usado para identificar exclusivamente um dispositivo.

Esse identificador também é usado quando o registro do dispositivo é cancelado temporariamente e, em seguida, registrado novamente. Quando um dispositivo é desregistrado temporariamente, o host do dispositivo não exclui o UDN. Os motivos para não excluir o UDN incluem:

-   O dispositivo está sendo atualizado.
-   Você está alterando as propriedades do dispositivo.
-   Um serviço está temporariamente indisponível.
-   Você está adicionando um novo serviço a um dispositivo.
-   Você está atualizando a DLL.
-   O dispositivo está em modo de espera.

Consulte as seções a seguir para obter mais informações sobre o registro:

-   [Como registrar um dispositivo no host do dispositivo](how-to-register-a-device-with-the-device-host.md)
-   [Cancelando o registro de um dispositivo](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




