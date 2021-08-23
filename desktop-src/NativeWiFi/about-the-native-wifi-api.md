---
description: A API Wi-Fi nativa contém funções, estruturas e enumerações que dão suporte à conectividade de rede sem fio e ao gerenciamento de perfil sem fio.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Sobre a API Wi-Fi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fafbe65d162668930470712c79637a41fcd0ee0769441b745e68bca156ada4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685456"
---
# <a name="about-the-native-wifi-api"></a>Sobre a API Wi-Fi nativa

A API Wi-Fi nativa contém funções, estruturas e enumerações que dão suporte à conectividade de rede sem fio e ao gerenciamento de perfil sem fio. A API pode ser usada para redes de infraestrutura e ad hoc. A API ad hoc sem fio é uma interface simplificada orientada a objeto para criar, gerenciar e usar redes ad hoc.

> [!Note]  
> O modo ad hoc pode não estar disponível em versões futuras do Windows. a partir do Windows 8.1 e do Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) em vez disso.

 

A implementação da API ad hoc usa a API Wi-Fi nativa. Isso significa que as chamadas de API ad hoc podem disparar notificações Wi-Fi nativas e vice-versa.

Misturar chamadas nativas à API WiFi e chamadas de API ad hoc sem fio não é recomendado. Os desenvolvedores devem escolher uma abordagem de programação antes de criar um aplicativo. Se seu aplicativo usar ou gerenciar redes de infraestrutura, você deverá usar a API Wi-Fi nativa. Se seu aplicativo exigir a funcionalidade de gerenciamento de perfil, você deverá usar a API Wi-Fi nativa. Caso contrário, você deve usar a API ad hoc sem fio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre WiFi nativo](about-native-wifi.md)
</dt> <dt>

[suporte nativo à API Wifi no Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Permissões nativas da API WiFi](native-wifi-api-permissions.md)
</dt> <dt>

[Sobre a API ad hoc sem fio](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[baixar o SDK do Windows Vista](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



