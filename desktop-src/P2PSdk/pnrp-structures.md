---
description: 'A API do provedor de namespace do PNRP usa as seguintes estruturas:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Estruturas PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756575"
---
# <a name="pnrp-structures"></a>Estruturas PNRP

A API do provedor de namespace do PNRP usa as seguintes estruturas:



| Estrutura                                                             | Descrição                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**informações de ponto de \_ extremidade PNRP par \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Contém os endereços IP e os dados associados a um ponto de extremidade par.                                                                                                 |
| [**\_informações de \_ nuvem \_ PNRP par**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Contém informações sobre uma nuvem PNRP (Peer Name Resolution Protocol).                                                                                            |
| [**\_informações de \_ registro de PNRP de pares \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Contém as informações fornecidas por uma identidade de par quando ele se registra em uma nuvem PNRP.                                                                           |
| [PNRP e BLOB](pnrp-and-blob.md)                                    | Passa dados para a estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) durante chamadas para várias funções.                                                  |
| [PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | Facilita a resolução de nomes e a enumeração de nomes e nuvens.                                                                                         |
| [**\_ID da nuvem PNRP \_**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Contém os valores que definem uma nuvem de rede.                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | Apontado pelo membro **lpBlob** da estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) .                                                            |
| [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | Apontado pelo membro **lpBlob** da estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md)                                                             |
| [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | Apontado pelo membro **lpBlob** da estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) e fornece suporte para dados opacos específicos do aplicativo. |



 

 

 
