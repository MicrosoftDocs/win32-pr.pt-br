---
description: A API Wi-Fi nativa contém funções, estruturas e enumerações que dão suporte à conectividade de rede sem fio e ao gerenciamento de perfil sem fio.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Sobre a API Wi-Fi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171686"
---
# <a name="about-the-native-wifi-api"></a>Sobre a API Wi-Fi nativa

A API Wi-Fi nativa contém funções, estruturas e enumerações que dão suporte à conectividade de rede sem fio e ao gerenciamento de perfil sem fio. A API pode ser usada para redes de infraestrutura e ad hoc. A API ad hoc sem fio é uma interface simplificada orientada a objeto para criar, gerenciar e usar redes ad hoc.

> [!Note]  
> O modo ad hoc pode não estar disponível em versões futuras do Windows. A partir do Windows 8.1 e do Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

A implementação da API ad hoc usa a API Wi-Fi nativa. Isso significa que as chamadas de API ad hoc podem disparar notificações Wi-Fi nativas e vice-versa.

Misturar chamadas nativas à API WiFi e chamadas de API ad hoc sem fio não é recomendado. Os desenvolvedores devem escolher uma abordagem de programação antes de criar um aplicativo. Se seu aplicativo usar ou gerenciar redes de infraestrutura, você deverá usar a API Wi-Fi nativa. Se seu aplicativo exigir a funcionalidade de gerenciamento de perfil, você deverá usar a API Wi-Fi nativa. Caso contrário, você deve usar a API ad hoc sem fio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre WiFi nativo](about-native-wifi.md)
</dt> <dt>

[Suporte nativo à API WiFi no Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Permissões nativas da API WiFi](native-wifi-api-permissions.md)
</dt> <dt>

[Sobre a API ad hoc sem fio](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Baixe o SDK do Windows Vista](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



