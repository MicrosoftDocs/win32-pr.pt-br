---
title: Sobre o NDF
description: O Estrutura de Diagnóstico de Rede (NDF) reduz o envolvimento de administradores de rede e usuários de computador ao lidar com problemas comuns de rede conforme eles ocorrem.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2ce4890645e83c27e9c1cf594d7fbf4d81ce3d662a2b470ce652c71e7d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798898"
---
# <a name="about-ndf"></a>Sobre o NDF

O Estrutura de Diagnóstico de Rede (NDF) reduz o envolvimento de administradores de rede e usuários de computador ao lidar com problemas comuns de rede conforme eles ocorrem. Usando os recursos de diagnóstico e reparo do NDF, os usuários e administradores não precisam de ferramentas adicionais para lidar com alguns problemas relativamente comuns. O NDF é Windows vista, Windows Server 2008 e posterior. Ele está disponível sempre que um sistema é inicializado (mas não pode ser executado no modo Cofre).

## <a name="ndf-helper-classes"></a>Classes auxiliares do NDF

O NDF inclui classes auxiliares que diagnosticam problemas de rede conforme eles ocorrem. Cada uma dessas classes auxiliares contém a lógica necessária para solucionar problemas de pelo menos um componente ou aplicativo.

Classes auxiliares individuais do NDF executam as tarefas primárias da sessão de diagnóstico. Cada classe auxiliar é uma unidade de código projetada para avaliar um aspecto de saúde de seu respectivo componente de rede. A classe auxiliar também entende quais opções de reparo possíveis estão disponíveis para restaurar a saúde do componente, bem como o custo e o risco de qualquer opção de reparo específica.

Cada classe auxiliar se conecta à classe geral Estrutura de Diagnóstico de Rede. Se um componente de rede de terceiros incluir uma classe auxiliar NDF, os problemas com esse componente poderão ser resolvidos por outros aplicativos usando o NDF, sem exigir que eles tenham qualquer conhecimento específico desse componente.

As classes auxiliares desenvolvidas pela Microsoft fornecem aos desenvolvedores de software a funcionalidade principal de diagnóstico e reparo. Também há um pequeno conjunto de APIs que os desenvolvedores podem usar para diagnosticar problemas de rede usando o NDF. Para obter mais informações, consulte [Funções NDF e](ndf-functions.md) Exemplo de [diagnóstico NDF](ndf-diagnostics-example.md).

## <a name="extensible-helper-classes"></a>Classes auxiliares extensíveis

Em alguns casos, a funcionalidade mais específica de diagnóstico e reparo pode ser fornecida por desenvolvedores de aplicativos.

Algumas das classes auxiliares NDF da Microsoft foram projetadas para serem estendidas para fornecer recursos adicionais de diagnóstico e reparo. Isso significa que os desenvolvedores podem incluir funcionalidades para usar os recursos de diagnóstico e reparo do NDF para solucionar problemas específicos de seu software ou hardware.

Por exemplo, a equipe sem fio da Microsoft fornece uma classe auxiliar extensível que permite que fornecedores sem fio de terceiros adicionem lógica de solução de problemas específica para seu hardware e/ou software específicos. Eles podem fazer isso desenvolvendo uma extensão de classe auxiliar do NDF. Para obter mais informações, consulte [802.11 Classes auxiliares extensíveis](802-11-wireless-diagnostics-extensible-helper-classes.md)de diagnóstico sem fio .

Uma extensão de classe auxiliar NDF, por definição, estende a funcionalidade de uma classe auxiliar extensível existente. Se uma classe auxiliar não for extensível, ninguém poderá escrever uma extensão para essa classe auxiliar.

## <a name="benefits-of-helper-class-extensions"></a>Benefícios das extensões de classe auxiliar

O NDF oferece várias vantagens distintas para incentivar seu uso por desenvolvedores de componentes de rede. Na parte superior da lista, os clientes do software fornecedor liberarão alguns de seus próprios recursos de solução de problemas e reduzirão o custo total de propriedade. Uma extensão de classe auxiliar bem escrita também oferece os seguintes benefícios:

-   Permite que uma equipe determine quando o componente não é a causa de um problema de conectividade. Por exemplo, a rede geralmente é responsabilizada por problemas de conectividade que não são, na verdade, o resultado de uma falha de componente de rede. Ao escrever uma extensão de classe auxiliar, uma equipe pode descartar com mais facilidade um componente específico como a causa de uma falha de conectividade.
-   Permite que uma equipe dia diagnosticar e depurar rapidamente um problema dentro do componente. O tempo gasto de depuração e solução de problemas poderá ser eliminado se uma classe auxiliar for escrita para executar todas as etapas de diagnóstico padrão que seriam necessárias de qualquer forma.
-   Elimina a necessidade de escrever e dar suporte a ferramentas específicas para diagnosticar problemas. Uma classe auxiliar pode ser o repositório central para as funcionalidades de diagnóstico de um componente e técnicas de coleta de informações.
-   Disponibiliza diagnósticos específicos do componente para aplicativos, sem exigir que eles tenham qualquer conhecimento direto sobre o componente.

 

 




