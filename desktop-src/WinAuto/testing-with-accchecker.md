---
title: Testando com AccChecker
description: Descreve o fluxo de trabalho de teste típico que incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- testando com AccChecker
- AccChecker, fluxo de trabalho de teste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498622"
---
# <a name="testing-with-accchecker"></a><span data-ttu-id="ae117-105">Testando com AccChecker</span><span class="sxs-lookup"><span data-stu-id="ae117-105">Testing with AccChecker</span></span>

<span data-ttu-id="ae117-106">O cenário a seguir descreve as etapas que você geralmente segue ao testar com AccChecker.</span><span class="sxs-lookup"><span data-stu-id="ae117-106">The following scenario describes the steps that you typically follow when testing with AccChecker.</span></span>

> [!Note]  
> <span data-ttu-id="ae117-107">Quando as rotinas de verificação AccChecker estão em execução, a interação do usuário com a máquina host pode interferir em algumas rotinas.</span><span class="sxs-lookup"><span data-stu-id="ae117-107">When AccChecker verification routines are running, user interaction with the host machine can interfere with some routines.</span></span> <span data-ttu-id="ae117-108">Recomendamos que nenhuma interação adicional do usuário ocorra até que o AccChecker notifique o usuário de que todas as tarefas foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="ae117-108">We recommend that no further user interaction occur until AccChecker notifies the user that all tasks are complete.</span></span>

 

1.  <span data-ttu-id="ae117-109">Execute as verificações de AccChecker em um aplicativo ou controle de destino específico.</span><span class="sxs-lookup"><span data-stu-id="ae117-109">Run AccChecker verifications on a particular target application or control.</span></span> <span data-ttu-id="ae117-110">Para obter mais informações, consulte a [guia verificações](the-accchecker-graphical-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ae117-110">For more information, see [Verifications Tab](the-accchecker-graphical-user-interface.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="ae117-111">AccChecker não explora todas as permutações de interface do usuário em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae117-111">AccChecker doesn't explore all UI permutations in an application.</span></span> <span data-ttu-id="ae117-112">Elementos ocultos em controles como Windows, painéis, guias e menus devem ser expostos manualmente.</span><span class="sxs-lookup"><span data-stu-id="ae117-112">Elements hidden within controls such as windows, panes, tabs, and menus must be exposed manually.</span></span>

     

2.  <span data-ttu-id="ae117-113">Examine o log de erros do AccChecker e avalie ou faça a triagem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="ae117-113">Examine the AccChecker error log and assess or triage the results.</span></span> <span data-ttu-id="ae117-114">Corrija problemas triviais e registre bugs graves conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="ae117-114">Fix trivial issues and log severe bugs as appropriate.</span></span>
3.  <span data-ttu-id="ae117-115">Gerar um arquivo de supressão para bugs e erros que podem ser ignorados até o teste de regressão.</span><span class="sxs-lookup"><span data-stu-id="ae117-115">Generate a suppression file for bugs and errors that can be ignored until regression testing.</span></span>
4.  <span data-ttu-id="ae117-116">Execute novamente as verificações de AccChecker com o arquivo de supressão e correções de bugs iniciais.</span><span class="sxs-lookup"><span data-stu-id="ae117-116">Re-run AccChecker verifications with the suppression file and initial bug fixes.</span></span> <span data-ttu-id="ae117-117">Isso fornece um instantâneo dos problemas na implementação atual do Microsoft Acessibilidade Ativa e estabelece uma linha de base para testes de regressão.</span><span class="sxs-lookup"><span data-stu-id="ae117-117">This provides a snapshot of the issues in the current implementation of Microsoft Active Accessibility and establishes a baseline for regression testing.</span></span>
5.  <span data-ttu-id="ae117-118">Integre as APIs do AccChecker e o arquivo de supressão em uma estrutura de teste automatizada para testes de regressão em log de bugs das verificações de AccChecker iniciais.</span><span class="sxs-lookup"><span data-stu-id="ae117-118">Integrate the AccChecker APIs and suppression file into an automated test framework for regression testing on bugs logged from the initial AccChecker verifications.</span></span>
    > [!Note]  
    > <span data-ttu-id="ae117-119">À medida que os bugs são corrigidos, o arquivo de supressão deve ser modificado conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="ae117-119">As bugs are fixed, the suppression file should be modified as required.</span></span>

     

6.  <span data-ttu-id="ae117-120">Confirme se nenhuma regressão ou novos bugs de acessibilidade foram introduzidos no aplicativo ou no controle.</span><span class="sxs-lookup"><span data-stu-id="ae117-120">Confirm that no regressions or new accessibility bugs have been introduced into the application or control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae117-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae117-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae117-122">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="ae117-122">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




