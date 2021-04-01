---
description: As interfaces de CRM são necessárias para fornecer suporte para trabalhadores de CRM e compensadores de CRM desenvolvidos usando Visual Basic e Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfaces do CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646526"
---
# <a name="com-crm-interfaces"></a>Interfaces do CRM COM+

As interfaces de CRM são necessárias para fornecer suporte para trabalhadores de CRM e compensadores de CRM desenvolvidos usando Visual Basic e Visual C++.

Você pode usar o CRM (Gerenciador de recursos de compensação COM+) para integrar com rapidez e facilidade recursos de aplicativos com transações do Microsoft Coordenador de Transações Distribuídas (DTC).

É mais fácil para os componentes escritos com Visual Basic criar um registro de log como uma coleção de variantes. Além disso, Visual Basic componentes são segmentados em apartamento, o que implica que deve ser possível realizar marshaling das interfaces do apartamento multithread para um apartamento de thread único. Os componentes do CRM desenvolvidos com o Visual C++ também podem usar o modelo de Threading Apartment, embora seja recomendável que eles usem o modelo de Threading em vez disso.

As interfaces descritas na tabela a seguir fornecem informações de referência detalhadas para desenvolvedores de COM+ CRMs.



| Interfaces do CRM                                             | Descrição                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | Essa interface fornece registros de log não estruturados em Visual C++.                                                           |
| [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | Essa interface fornece registros de log estruturados para o compensador de CRM ao usar o Visual Basic.                            |
| [**ICrmFormatLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | Essa interface converte os registros de log no formato exibível para que eles possam ser apresentados usando uma ferramenta de monitoramento genérica. |
| [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | Essa interface é usada pelo compensador CRM e CRM para gravar registros no log e torná-los duráveis.           |
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | Essa interface captura um instantâneo do estado atual de um CRM e mantém um funcionário específico do CRM.                          |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | Essa interface obtém informações sobre o estado dos auxiliares.                                                             |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | Essa interface monitora os registros de log individuais mantidos por um vendedor de CRM específico para uma determinada transação.            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



