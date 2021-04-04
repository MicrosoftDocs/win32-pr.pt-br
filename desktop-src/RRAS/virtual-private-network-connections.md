---
title: Conexões de rede virtual privada
description: O RAS (serviço de acesso remoto) dá suporte a conexões de VPN (rede virtual privada), além de conexões de acesso remoto convencionais que usam o protocolo PPP (PPP).
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f5fc0b80a6eb00e7587e941eea39c056a11d14
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007662"
---
# <a name="virtual-private-network-connections"></a>Conexões de rede virtual privada

O RAS (serviço de acesso remoto) dá suporte a conexões de VPN (rede virtual privada), além de conexões de acesso remoto convencionais que usam o protocolo PPP (PPP). Em uma conexão VPN, os pacotes de VPN são encapsulados em pacotes IP e enviados por uma rede IP, como a Internet. Portanto, o acesso a uma rede IP é um requisito para estabelecer uma conexão VPN. Se o computador cliente tiver uma conexão sempre ativa com uma rede IP, por exemplo, uma conexão com uma LAN IP, o cliente poderá estabelecer a conexão VPN usando uma única chamada para a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .

Se o computador cliente não tiver uma conexão sempre ativa com uma rede IP, duas chamadas para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) serão necessárias para estabelecer a conexão VPN. A primeira chamada estabelece uma conexão discada à rede IP; a segunda chamada estabelece a conexão VPN.

O membro **szLocalPhoneNumber** da estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para a conexão VPN deve conter o nome DNS ou o endereço IP do servidor VPN de destino.

Cada conexão requer uma entrada [de catálogo telefônico](ras-phone-books.md) separada. A primeira chamada para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica a entrada do catálogo telefônico para a rede IP. A segunda chamada especifica a entrada do catálogo telefônico para a VPN.

A função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) usa um ponteiro para uma estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) como um parâmetro. Essa estrutura especifica as credenciais de autenticação a serem usadas para a rede especificada pela entrada do catálogo telefônico. As credenciais necessárias para acessar a rede IP são normalmente diferentes daquelas da VPN. A primeira chamada para **RasDial** deve especificar credenciais para a rede IP. A segunda chamada deve especificar as credenciais para a VPN.

Se a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) for bem-sucedida, ela retornará um identificador para a conexão. Use esse identificador em uma chamada para [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para encerrar a conexão.

No cenário anterior, as duas chamadas para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) retornam identificadores de conexão separados para a rede IP e a VPN. Chamar [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) com o identificador para a conexão VPN encerra a conexão VPN, mas deixa a conexão com a rede IP intacta.

 

 