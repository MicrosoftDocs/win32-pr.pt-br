---
description: Windows Solução de segurança de família
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Windows Solução de segurança de família
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5e5749201fc849e7c9476c97c6fbd3dc5ee5b2d3f26ed3988eb72ac59c1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951646"
---
# <a name="windows-family-safety-solution"></a>Windows Solução de segurança de família

Os principais requisitos definidos pela Microsoft para uma solução mais abrangente são os seguintes. Observe que a definição para online é basicamente uma tecnologia voltada para a Internet, ao contrário de um cliente offline, que geralmente é associado ao computador.

-   Forneça uma área única e fácil de localizar na interface do usuário do sistema operacional, em que todas as políticas de controles dos pais, controle de monitoramento de atividades e dados de atividade de uma identidade podem ser prontamente descobertas.

-   Dá suporte ao monitoramento de atividade suficiente do usuário controlado para que um pai ou guardião tenha a confiança razoável de que atividades arriscadas podem ser descobertas. Além disso, a reconfiguração de log das políticas do usuário controlado para que as alterações involuntárias ou não autorizadas sejam detectáveis.

-   expor recursos de monitoramento de atividade por meio de interfaces de log de eventos do Windows Vista standard e forneça uma solução de visualizador na caixa. Defina eventos de atividade padrão e forneça a extensibilidade para a geração de eventos personalizados por ISVs.

-   Promova que todo o monitoramento e as restrições de um usuário sejam ativados apenas em uma base de aceitação por pais ou tutores. Sempre que possível, a funcionalidade de restrições deve estar completamente inativa para usuários não controlados para minimizar os riscos de segurança e compatibilidade de aplicativos.

-   A Microsoft deve se esforçar, sempre que possível, não fazer julgamentos de valor por idade ou outros parâmetros para o usuário controlado (terceiros podem optar por fazer isso). Essas decisões são deixadas para o pai ou o guardião, geralmente influenciadas por comunidades ou organizações.

-   Forneça implementações no produto para monitoramento de atividade offline e restrições em que algumas ou nenhuma oferta está disponível atualmente, em que a funcionalidade de risco de segurança associada está disponível no produto ou em que uma solução da Microsoft fornece funcionalidades compatíveis e robustas totalmente integradas ao design do sistema operacional.

-   Em geral, promova os aplicativos que executam seu próprio registro em log e restrições para melhor experiência de contexto e interface do usuário.

    Exceção: forneça monitoramento e restrições de atividades online abrangentes em áreas selecionadas em que o benefício para os consumidores e o setor superar os custos.

-   exponha as configurações de interface do usuário de controles e definições de eventos de atividade usando APIs públicas para que terceiros possam consultar o estado, modificar configurações e ler logs de atividades se estiverem executando com privilégios de conta Windows suficientes.

Uma meta abrangente é promover a coexistência de soluções de controles pais de terceiros com a funcionalidade interna e dar suporte à agregação de valor por meio da integração com, extensão ou fornecimento de recursos alternativos quando adequado.

 

 



