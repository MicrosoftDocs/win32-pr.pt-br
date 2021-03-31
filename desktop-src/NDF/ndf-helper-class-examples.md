---
title: Exemplos de extensão de classe auxiliar NDF
description: Esses exemplos se aplicam somente quando os desenvolvedores acreditam que é necessário estender a funcionalidade de uma classe auxiliar NDF da Microsoft que é declarada para ser extensível.
ms.assetid: 048e42f5-66d8-41c6-9e97-8da68c9ad151
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3ecf34bb8e90aad8c28f582860d44e81706e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634759"
---
# <a name="ndf-helper-class-extension-examples"></a><span data-ttu-id="1617c-103">Exemplos de extensão de classe auxiliar NDF</span><span class="sxs-lookup"><span data-stu-id="1617c-103">NDF Helper Class Extension Examples</span></span>

<span data-ttu-id="1617c-104">Esses exemplos se aplicam somente quando os desenvolvedores acreditam que é necessário estender a funcionalidade de uma classe auxiliar NDF da Microsoft que é declarada para ser extensível.</span><span class="sxs-lookup"><span data-stu-id="1617c-104">These examples apply only when developers believe it is necessary to extend the functionality of a Microsoft NDF Helper Class that is declared to be extensible.</span></span> <span data-ttu-id="1617c-105">Isso geralmente não é necessário, mas, em alguns casos, oportunidades de diagnóstico exclusivas se apresentam devido aos requisitos específicos de hardware ou software do componente.</span><span class="sxs-lookup"><span data-stu-id="1617c-105">This is generally not necessary, but in some cases, unique diagnostic opportunities present themselves because of the specific hardware or software requirements of the component.</span></span>

<span data-ttu-id="1617c-106">Os dois exemplos a seguir estão relacionados e o primeiro deve ser compreendido antes da análise do segundo.</span><span class="sxs-lookup"><span data-stu-id="1617c-106">The two examples that follow are related and the first should be understood before analyzing the second.</span></span> <span data-ttu-id="1617c-107">A primeira fornece uma implementação de uma [extensão de classe auxiliar NDF](ndf-helper-class-example.md) usando uma classe chamada SimpleHelperFileClass.</span><span class="sxs-lookup"><span data-stu-id="1617c-107">The first provides an implementation of an [NDF Helper Class Extension](ndf-helper-class-example.md) using a class called SimpleHelperFileClass.</span></span>

<span data-ttu-id="1617c-108">A segunda, [extensão de classe auxiliar NDF com entrega](ndf-helper-class-example-with-handoff.md), fornece um exemplo de uma extensão que não executa tarefas de diagnóstico específicas, mas gera apenas uma hipótese de integridade baixa para o SimpleHelperFileClass no primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="1617c-108">The second, [NDF Helper Class Extension with Handoff](ndf-helper-class-example-with-handoff.md), provides an example of an extension that does not perform specific diagnostic tasks but only generates a low health hypothesis for the SimpleHelperFileClass in the first example.</span></span>

 

 




