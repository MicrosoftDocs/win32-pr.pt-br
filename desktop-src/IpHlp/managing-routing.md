---
description: O IP Helper fornece recursos para gerenciar o roteamento de rede. Use as funções a seguir para gerenciar a tabela de roteamento de IP e para obter outras informações de roteamento.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Gerenciando o roteamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827048"
---
# <a name="managing-routing"></a>Gerenciando o roteamento

O IP Helper fornece recursos para gerenciar o roteamento de rede. Use as funções a seguir para gerenciar a tabela de roteamento de IP e para obter outras informações de roteamento.

Recupere o conteúdo da tabela de roteamento de IP fazendo uma chamada para a função [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) . Manipule entradas específicas na tabela de roteamento de IP usando as funções [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)e [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) . Use a função **CreateIpForwardEntry** para adicionar uma nova entrada da tabela de roteamento. Use a função **DeleteIpForwardEntry** para remover uma entrada existente. A função **SetIpForwardEntry** modifica uma entrada existente.

Os recursos de gerenciamento de roteador do auxiliar de IP podem ser usados para recuperar informações sobre como os datagramas são roteados pela rede. A função [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera a melhor rota para um endereço de destino especificado. A função [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera o índice da interface usada pela melhor rota para um endereço de destino especificado. Por fim, a função [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) recupera o tempo de ida e volta (RTT) e o número de saltos para um endereço de destino especificado.

 

 



