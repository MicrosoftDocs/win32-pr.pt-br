---
title: Registro em log (plataforma de filtragem do Windows)
description: A WFP (Windows Filtering Platform) fornece registro em log de quedas de pacotes e falhas de IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105757163"
---
# <a name="logging-windows-filtering-platform"></a>Registro em log (plataforma de filtragem do Windows)

A WFP (Windows Filtering Platform) fornece registro em log de quedas de pacotes e falhas de IKE/AuthIP.

Os eventos registrados são definidos no tipo enumerado [**\_ tipo de \_ evento \_ FWPM net**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) e são os seguintes.

-   Falhas no modo principal IKE/AuthIP.
-   Falhas de modo rápido IKE/AuthIP.
-   Falhas de modo estendido AuthIP.
-   Pacotes removidos durante a classificação.
-   Pacotes removidos pelo IPsec.

Por padrão, o log para WFP é habilitado para pacotes de entrada unicast e para todos os pacotes de saída (unicast, multicast e difusão). O registro em log pode ser habilitado para o restante dos pacotes ou desabilitado para todos os pacotes, por meio da função de gerenciamento [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) . As configurações de evento persistem entre reinicializações.

Os eventos registrados são armazenados em um log circular, que são novos eventos que substituem os antigos quando o log atinge seu tamanho máximo e podem ser analisados usando as funções de [Gerenciamento de eventos](fwp-mgmt-functions.md) fornecidas pela WFP. O log de eventos tem um tamanho máximo de 128 KB e pode conter cerca de 100 a 150 eventos.

As funções de enumeração em geral e [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) em particular fazem um instantâneo do log no momento em que o identificador de enumeração é criado. As chamadas subsequentes usando o mesmo identificador de enumeração retornam o próximo conjunto de itens após aqueles no último buffer de saída.

Quando um aplicativo desabilita o log de WFP (chamando [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), todos os aplicativos são afetados. O log de eventos não é limpo até que um aplicativo habilite novamente o log WFP, mas o log de eventos não pode ser consultado antes.

O log de eventos do WFP é esvaziado após uma reinicialização.

 

 




