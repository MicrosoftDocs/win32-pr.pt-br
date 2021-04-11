---
description: A infraestrutura de CRM fornece um conjunto de interfaces que podem ser usadas para monitorar o CRMs em um determinado aplicativo de servidor.
ms.assetid: b8f40c91-001b-4003-b377-57a918988100
title: Interfaces de monitoramento do COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c893040c46810c980c647cbacdc808200e8d5f5e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163970"
---
# <a name="com-crm-monitoring-interfaces"></a>Interfaces de monitoramento do COM+ CRM

A infraestrutura de CRM fornece um conjunto de interfaces que podem ser usadas para monitorar o CRMs em um determinado aplicativo de servidor. Para acessar as interfaces de monitoramento, um componente em execução no aplicativo do servidor deve primeiro criar um administrador de CRM especializado chamado administrador de recuperação do CRM.

No uso normal de CRMs, espera-se que as transações sejam de curta duração e, portanto, os trabalhadores do CRM e os recompensas de CRM existem por um breve período de tempo, normalmente apenas alguns segundos no máximo. As interfaces de monitoramento, portanto, são projetadas para fornecer um instantâneo do estado do CRMs em execução em um determinado ponto no tempo. Se qualquer um dos CRMs estiver tendo problemas, as interfaces de monitoramento poderão ser usadas para zero no CRM problemático, para inspecionar seus registros de log e para anular sua transação, se necessário.

A seguir estão as três interfaces de monitoramento de CRM e as descrições de como elas funcionam.



| Interface                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)<br/>                     | Usando [**ICrmMonitor::**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-getclerks)getadministradores, um instantâneo pode ser obtido do conjunto atual de administradores do Active Directory dentro do aplicativo do servidor. A partir disso, um objeto de coleção de funcionário do CRM de interesse específico pode ser localizado e consultado, incluindo o estado atual de sua transação e os registros de log gravados pelo CRM.<br/> Quando a ferramenta de monitoramento determinou qual administrador é interessante, ela chama [**ICrmMonitor:: HoldClerk**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-holdclerk) para obter uma interface [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) nesse administrador específico. Neste ponto, a ferramenta de monitoramento está mantendo uma referência a esse administrador e, se a transação for concluída, o auxiliar será mantido na memória e não será liberado até que a ferramenta de monitoramento seja feita.<br/>                                                                                                                                                                                                    |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)<br/>         | Usando essa interface, o objeto de coleção do auxiliar pode ser procurado por informações sobre o estado da coleção do auxiliar no momento em que foi obtido. Essas informações incluem o número de auxiliares, o ProgID do compensador de CRM usado pelo administrador, a descrição fornecida no momento em que o compensador de CRM foi registrado (usando [**ICrmLogControl:: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator)), a ID da unidade de trabalho da transação e a ID da atividade. Os auxiliares individuais também são identificados exclusivamente por um "CLSID da instância do auxiliar", que não é um CLSID do COM no sentido normal do termo, mas simplesmente um GUID exclusivo que identifica esse determinado funcionário durante seu tempo de vida.<br/>                                                                                                                                                                                                                                                                                                |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)<br/> | Essa interface pode ser usada para consultar o estado atual da transação, para descobrir quantos registros de log esse administrador do CRM escreveu e obter os dados reais de registro de log. Os registros de log são fornecidos da interface [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) no mesmo formato em que foram gravados originalmente (usando [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)). Além disso, o **ICrmMonitorLogRecords** pode ser implementado opcionalmente para converter os registros de log em formato exibível para que possam ser apresentados usando uma ferramenta de monitoramento genérica.<br/> Como o [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) é implementado diretamente no administrador do CRM, você pode [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) (também implementado no administrador do CRM). Isso pode ser usado para anular a transação diretamente, se necessário ([**ICrmLogControl:: ForceTransactionToAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcetransactiontoabort)).<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

