---
description: 'O modelo conceitual: requisitos de aplicativo'
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 'O modelo conceitual: requisitos de aplicativo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19c69f8da7179765242815c4d01760c36b94e95714188f7db772600826d0416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853916"
---
# <a name="the-conceptual-model-application-requirements"></a>O modelo conceitual: requisitos de aplicativo

Ao projetar o modelo conceitual, você precisa definir os problemas de negócios e as funções necessárias para resolver esses problemas. Uma abordagem de práticas recomendadas é conversar com pessoas que realmente usarão o aplicativo, atender a uma ampla variedade de usuários e incluir o máximo possível de cenários de negócios ou usuários. Determine as identidades e o número de usuários potenciais do sistema, bem como o tamanho e o escopo dos dados envolvidos. Embora a coleta dessas informações possa ser o aspecto menos técnico do processo de design, ela é um dos mais importantes. Para desenvolver um aplicativo bem-sucedido, você precisa ter uma compreensão clara dos problemas de negócios e dos processos que precisam ser resolvidos.

Ao determinar os requisitos do aplicativo, tenha as seguintes considerações em mente:

-   Requisitos de desempenho. Qual é o tempo de resposta esperado para tarefas de aplicativo? Qual suporte de failover para servidores inocessados é necessário? Quais são as horas de disponibilidade?
-   Ambiente. Quais servidores estão disponíveis? Os servidores adicionais estão planejados para lidar com os requisitos de dimensionamento?
-   Implantação. Como o aplicativo se integrará a um sistema atual? Com quais outros sistemas o aplicativo interagirá? Quais sistemas operacionais os outros sistemas usam? Quais protocolos de comunicação devem ter suporte? Qual API você pode usar para interagir com os outros sistemas? Onde estão os outros sistemas localizados na rede? Quais restrições de uso do computador estão em uso? Quais contas de usuário têm permissão de acesso?
-   Local. Onde os dados estão localizados em relação ao cliente? Os dados são acessados remotamente ou são locais?
-   Segurança. Há requisitos de verificação de integridade ou criptografia? Há requisitos de autenticação ou proteção de dados?
-   Direitos de acesso. Há restrições sobre quem tem permissão para executar determinadas operações? Nesse caso, você deve primeiro documentar quais operações exigem autorização e, em seguida, documentar os tipos de usuários que podem ter autorização. Esses requisitos podem ter um grande impacto sobre como as partes do aplicativo são implementadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo lógico: definição e planejamento de aplicativos](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[O modelo físico: arquitetura do aplicativo](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



