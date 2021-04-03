---
description: Os NPPs (provedores de pacotes de rede) são Monitor de Rede componentes do sistema que coletam o tráfego de rede (quadros) da rede e os transmitem para a interface do usuário do Monitor de Rede e para os aplicativos do NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Provedores de pacotes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837292"
---
# <a name="network-packet-providers"></a>Provedores de pacotes de rede

Os NPPs (provedores de pacotes de rede) são Monitor de Rede componentes do sistema que coletam o tráfego de rede (quadros) da rede e os transmitem para a interface do usuário do Monitor de Rede e para os [*aplicativos do NPP*](n.md).

A ilustração a seguir mostra dois NPPs: o NPP de NDIS fornecido pelo Monitor de Rede e um NPP personalizado.

![NPP NDIS fornecidos pelo monitor de rede e um NPP personalizado](images/npp.png)

O NPP NDIS fornecido pelo Monitor de Rede é Ndisnpp.dll. Esse NPP usa o Nmnt.sys (driver de sistema Monitor de Rede) para obter os quadros coletados da rede e várias interfaces COM (chamadas de interfaces NPP) para passar os quadros para a interface do usuário do Monitor de Rede e para os aplicativos NPP, nos quais eles podem ser exibidos e analisados.

Ndisnpp.dll conecta-se à camada [*NDIS*](n.md) para obter seu tráfego de rede. (O NPPs personalizado pode ignorar a camada NDIS e se comunicar diretamente com o hardware de rede.) Lembre-se de que, independentemente de um NPP usar o NDIS, o NPPs pode se conectar a qualquer número de placas de rede e que todas as NPPs devem oferecer suporte às mesmas interfaces NPP.

Antes que um aplicativo possa começar a capturar dados, ele deve:

-   Selecione a placa de interface de rede (NIC) que conectará o NPP à rede.
-   Selecione a interface NPP que será usada para capturar os quadros de rede.
-   Use a interface selecionada para se conectar à NIC.

Para obter mais informações sobre como enumerar e selecionar uma placa de interface de rede, consulte [selecionando uma placa de interface de rede](selecting-a-network-interface-card.md).

Para obter mais informações sobre interfaces COM expostas por NPPs, consulte [selecionando uma interface NPP](selecting-an-npp-interface.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStats**](istats.md)
</dt> </dl>

 

 



