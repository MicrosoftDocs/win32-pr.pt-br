---
title: Registro em log (Windows de Filtragem)
description: Windows A WFP (Plataforma de Filtragem) fornece registro em log de quedas de pacotes e falhas de IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1500be04837126e6907b663e4496c58c05380d313a1465b9c8db05b5ea39d832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068906"
---
# <a name="logging-windows-filtering-platform"></a>Registro em log (Windows de Filtragem)

O Windows WFP (Plataforma de Filtragem de Dados) fornece registro em log de quedas de pacotes e falhas de IKE/AuthIP.

Os eventos registrados são definidos no tipo enumerado [**FWPM \_ NET \_ EVENT \_ TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) e são da seguinte forma.

-   Falhas no modo principal IKE/AuthIP.
-   Falhas no modo rápido IKE/AuthIP.
-   Falhas no modo estendido do AuthIP.
-   Pacotes descartados durante a classificação.
-   Pacotes descartados pelo IPsec.

Por padrão, o registro em log para WFP é habilitado para pacotes de entrada unicast e para todos os pacotes de saída (unicast, multicast e difusão). O registro em log pode ser habilitado para o restante dos pacotes ou desabilitado para todos os pacotes, por meio da função de gerenciamento [**FwpmEngineSetOptions0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) As configurações de evento persistem entre reinicializações.

Os eventos registrados em log são armazenados em um log circular, ou seja, novos eventos [](fwp-mgmt-functions.md) substituem os antigos quando o log atinge seu tamanho máximo e podem ser analisados usando as funções de gerenciamento de eventos fornecidas pelo WFP. O log de eventos tem um tamanho máximo de 128 KB e pode conter cerca de 100 a 150 eventos.

Funções de enumeração em geral e [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) em particular, tirar um instantâneo do log no momento em que o alça de enumeração for criado. Chamadas subsequentes que usam o mesmo alça de enumeração retornam o próximo conjunto de itens após aqueles no último buffer de saída.

Quando um aplicativo desabilita o registro em log do WFP (chamando [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), todos os aplicativos são afetados. O log de eventos não é limpo até que um aplicativo habilita o registro em log do WFP, mas o log de eventos não pode ser consultado antes disso.

O log de eventos do WFP é esvaziado após uma reinicialização.

 

 




