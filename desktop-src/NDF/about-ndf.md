---
title: Sobre NDF
description: O NDF (estrutura de diagnóstico de rede) reduz o envolvimento dos administradores de rede e dos usuários de computador ao lidar com problemas comuns de rede à medida que eles ocorrem.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b638298fe321d314815c74fced49d3dfb623022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635665"
---
# <a name="about-ndf"></a>Sobre NDF

O NDF (estrutura de diagnóstico de rede) reduz o envolvimento dos administradores de rede e dos usuários de computador ao lidar com problemas comuns de rede à medida que eles ocorrem. Usando os recursos de diagnóstico e reparo do NDF, os usuários e os administradores não precisam de ferramentas adicionais para lidar com alguns problemas relativamente comuns. O NDF é fornecido como parte do Windows Vista, do Windows Server 2008 e posterior. Ele está disponível sempre que um sistema é inicializado (mas não pode ser executado no modo de segurança).

## <a name="ndf-helper-classes"></a>Classes auxiliares NDF

O NDF inclui classes auxiliares que diagnosticam problemas de rede à medida que ocorrem. Cada uma dessas classes auxiliares contém a lógica necessária para solucionar problemas de pelo menos um componente ou aplicativo.

As classes individuais auxiliares do NDF executam as tarefas principais da sessão de diagnóstico. Cada classe auxiliar é uma unidade de código criada para avaliar um aspecto de integridade de seu respectivo componente de rede. A classe auxiliar também entende quais possíveis opções de reparo estão disponíveis para restaurar a integridade do componente, bem como o custo e o risco de qualquer opção de reparo específica.

Cada classe auxiliar se conecta à estrutura de diagnóstico de rede geral. Se um componente de rede de terceiros incluir uma classe auxiliar NDF, os problemas com esse componente poderão ser resolvidos por outros aplicativos que usam o NDF, sem a necessidade de ter qualquer conhecimento específico desse componente.

As classes auxiliares desenvolvidas pela Microsoft fornecem aos desenvolvedores de software a funcionalidade principal de diagnóstico e reparo. Também há um pequeno conjunto de APIs que os desenvolvedores podem usar para diagnosticar problemas de rede usando NDF. Para obter mais informações, consulte [funções NDF](ndf-functions.md) e [exemplo de diagnóstico NDF](ndf-diagnostics-example.md).

## <a name="extensible-helper-classes"></a>Classes auxiliares extensíveis

Em alguns casos, uma funcionalidade mais específica de diagnóstico e reparo pode ser fornecida por desenvolvedores de aplicativos.

Algumas das classes auxiliares NDF da Microsoft foram projetadas para serem estendidas para fornecer recursos adicionais de diagnóstico e reparo. Isso significa que os desenvolvedores podem incluir funcionalidade para usar recursos de diagnóstico e reparo NDF para solucionar problemas específicos de seu software ou hardware.

Por exemplo, a equipe sem fio da Microsoft fornece uma classe auxiliar extensível que permite que qualquer fornecedor sem fio de terceiros adicione lógica de solução de problemas específica para seu hardware e/ou software específico. Eles podem fazer isso desenvolvendo uma extensão de classe auxiliar NDF. Para obter mais informações, consulte [classes auxiliares extensível de diagnóstico sem fio 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md).

Uma extensão de classe auxiliar NDF, por definição, estende a funcionalidade de uma classe auxiliar extensível existente. Se uma classe auxiliar não for extensível, ninguém poderá gravar uma extensão para essa classe auxiliar.

## <a name="benefits-of-helper-class-extensions"></a>Benefícios das extensões de classe auxiliar

O NDF oferece várias vantagens distintas para incentivar seu uso por desenvolvedores de componentes de rede. Na parte superior da lista, os clientes do software do fornecedor liberarão alguns dos seus próprios recursos de solução de problemas e reduzirão o custo total de propriedade. Uma extensão de classe auxiliar bem escrita também oferece os seguintes benefícios:

-   Permite que uma equipe determine quando o componente não é a causa de um problema de conectividade. Por exemplo, geralmente a rede é culpada por problemas de conectividade que não são, na verdade, o resultado de uma falha de componente de rede. Ao escrever uma extensão de classe auxiliar, uma equipe pode facilmente eliminar um componente específico como a causa de uma falha de conectividade.
-   Permite que uma equipe diagnostique e depure rapidamente um problema dentro do componente. O tempo gasto na depuração e solução de problemas pode ser eliminado se uma classe auxiliar for gravada para executar todas as etapas de diagnóstico padrão que seriam exigidas de qualquer forma.
-   Elimina a necessidade de escrever e dar suporte a ferramentas one-off para diagnosticar problemas. Uma classe auxiliar pode ser o repositório central para os recursos de diagnóstico de um componente e técnicas de coleta de informações.
-   Torna o diagnóstico específico de componentes disponível para aplicativos, sem exigir que eles tenham qualquer conhecimento direto sobre o componente.

 

 




