---
title: Conexões de rede virtual privada
description: O RAS (Serviço de Acesso Remoto) dá suporte a conexões VPN (Rede Virtual Privada), além de conexões de acesso remoto convencionais que usam PROTOCOLO PPP (PPP).
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc532d0873a5c3cb4a50552ca267a8a88b305ad855a1588338786881b3af04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024776"
---
# <a name="virtual-private-network-connections"></a>Conexões de rede virtual privada

O RAS (Serviço de Acesso Remoto) dá suporte a conexões VPN (Rede Virtual Privada), além de conexões de acesso remoto convencionais que usam PROTOCOLO PPP (PPP). Em uma conexão VPN, os pacotes VPN são encapsulados em pacotes IP e enviados por uma rede IP, como a Internet. Portanto, o acesso a uma rede IP é um requisito para estabelecer uma conexão VPN. Se o computador cliente tiver uma conexão always-on com uma rede IP, por exemplo, uma conexão com uma LAN IP, o cliente poderá estabelecer a conexão VPN usando uma única chamada para a [**função RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Se o computador cliente não tiver uma conexão always-on com uma rede IP, duas chamadas para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) serão necessárias para estabelecer a conexão VPN. A primeira chamada estabelece uma conexão discar com a rede IP; a segunda chamada estabelece a conexão VPN.

O **membro szLocalPhoneNumber** da estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para a conexão VPN deve conter o nome DNS ou o endereço IP do servidor VPN de destino.

Cada conexão requer uma entrada [de lista telefônica](ras-phone-books.md) separada. A primeira chamada para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica a entrada de phone-book para a rede IP. A segunda chamada especifica a entrada de phone-book para a VPN.

A [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) leva um ponteiro para uma [**estrutura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) como um parâmetro. Essa estrutura especifica as credenciais de autenticação a usar para a rede especificada pela entrada de phone-book. As credenciais necessárias para acessar a rede IP normalmente são diferentes daquelas da VPN. A primeira chamada para **RasDial** deve especificar credenciais para a rede IP. A segunda chamada deve especificar credenciais para a VPN.

Se a [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) for bem-sucedida, ela retornará um handle para a conexão. Use esse handle em uma chamada para [**RasUp para**](/windows/desktop/api/Ras/nf-ras-rashangupa) encerrar a conexão.

No cenário anterior, as duas chamadas para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) retornam alças de conexão separadas para a rede IP e a VPN. Chamar [**RasVpnUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) com o handle para a conexão VPN encerra a conexão VPN, mas deixa a conexão com a rede IP intacta.

 

 