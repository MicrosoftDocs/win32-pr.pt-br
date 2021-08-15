---
description: 'A API do Provedor de Namespace PNRP usa as seguintes estruturas:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Estruturas PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e275dff1b0c0986cfa998ed64cfb1ffad5b19af400f8719715d2106af353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011524"
---
# <a name="pnrp-structures"></a>Estruturas PNRP

A API do Provedor de Namespace PNRP usa as seguintes estruturas:



| Estrutura                                                             | Descrição                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMAÇÕES \_ DE PONTO DE EXTREMIDADE \_ \_ PNRP PAR**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Contém os endereços IP e os dados associados a um ponto de extremidade par.                                                                                                 |
| [**INFORMAÇÕES DE \_ NUVEM PNRP \_ \_ PAR**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Contém informações sobre uma nuvem do PROTOCOLO PNRP.                                                                                            |
| [**INFORMAÇÕES DE \_ REGISTRO DE PNRP \_ \_ PAR**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Contém as informações fornecidas por uma identidade de par quando ele se registra em uma nuvem PNRP.                                                                           |
| [PNRP e BLOB](pnrp-and-blob.md)                                    | Passa dados para a [**estrutura WSAQUERYSET**](winsock-nsp-reference-links.md) durante chamadas para várias funções.                                                  |
| [PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | Facilita a resolução de nomes e a enumeração de nomes e nuvens.                                                                                         |
| [**ID DE \_ NUVEM PNRP \_**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Contém os valores que definem uma nuvem de rede.                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | Apontado pelo membro **lpBlob** da [**estrutura WSAQUERYSET.**](winsock-nsp-reference-links.md)                                                            |
| [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | Apontado pelo membro **lpBlob** da [**estrutura WSAQUERYSET**](winsock-nsp-reference-links.md)                                                             |
| [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | Apontado pelo membro **lpBlob** da estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) e dá suporte a dados opacos específicos do aplicativo. |



 

 

 
