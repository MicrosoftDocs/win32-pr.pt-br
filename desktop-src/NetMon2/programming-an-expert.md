---
description: O SDK do Monitor de Rede inclui as funções e o código de exemplo que você precisa para criar especialistas. No entanto, você também pode usar as ferramentas existentes, incluindo um editor de caixa de diálogo.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programando um especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091527"
---
# <a name="programming-an-expert"></a>Programando um especialista

O SDK do Monitor de Rede inclui as funções e o código de exemplo que você precisa para criar especialistas. No entanto, você também pode usar as ferramentas existentes, incluindo um editor de caixa de diálogo.

## <a name="minimum-requirements-to-run-an-expert"></a>Requisitos mínimos para executar um especialista

A tabela a seguir lista os pontos de entrada da DLL e as funções de especialista que você deve usar para criar um especialista.



| Nome                                                 | Type               | Obrigatório?                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [**DllMain**](dllmain-expert.md)                    | Função de entrada de DLL | Sim                                             |
| [**Registrar especialista**](register-expert.md)           | Função de entrada de DLL | Sim                                             |
| [**Executar**](run.md)                                   | Função de entrada de DLL | Sim                                             |
| [**Configurar**](configure.md)                       | Função de entrada de DLL | Somente se o especialista fornecer a configuração do usuário. |
| [**ExpertIndicateStatus**](expertindicatestatus.md) | Função de especialista    | Sim                                             |
| [**ExpertSubmitEvent**](expertsubmitevent.md)       | Função de especialista    | Sim                                             |



 

Examine os tópicos de referência do Expert e do parser no SDK do Monitor de Rede para atualizar seu código-fonte e, em seguida, use o código de exemplo e os procedimentos fornecidos nestes tópicos:

-   [Criando um especialista](building-an-expert.md)
-   [Instalando um especialista](installing-an-expert-to-network-monitor-2-1.md)
-   [Depurando um especialista](debugging-an-expert.md)

As DLLs de especialistas exigem o C, não o C++, a Convenção de chamada porque as funções são chamadas por meio de ponteiros de função usando uma sobreposição. Por meio de um conjunto de funções especialistas especializadas, o especialista tem acesso aos quadros na captura. O especialista pode usar a maior parte da API de Monitor de Rede para manipular os dados retornados. Quando um especialista encontra informações para enviar ao usuário, ele empacota as informações em uma estrutura de dados de evento e a envia para Monitor de Rede, que, em seguida, exibe as informações em uma janela de saída de especialista. O especialista deve atualizar periodicamente Monitor de Rede com informações de status de conclusão de porcentagem, que é fornecida pela função [**ExpertIndicateStatus**](expertindicatestatus.md) .

As funções exportadas do especialista são chamadas da seguinte maneira:

-   Quando Monitor de Rede está criando a lista de especialistas para apresentar ao usuário, Monitor de Rede chama a função de [**especialista de registro**](register-expert.md) .
-   Após a chamada para o **registro**, se o especialista for configurável, monitor de rede chamará a função [**Configurar**](configure.md) .
-   Quando o usuário Monitor de Rede clica em **executar especialista**, monitor de rede chama a função [**executar**](run.md) .

Quando os especialistas analisam os quadros solicitados e encontram um problema, eles usam o [**ExpertSubmitEvent**](expertsubmitevent.md) para enviar um evento que contém informações sobre o problema. Monitor de Rede distribui o evento para o Visualizador de Eventos padrão (compartilhado) ou (se o especialista o registra) em uma Visualizador de Eventos privada.

 

 



