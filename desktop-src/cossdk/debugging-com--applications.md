---
description: As técnicas de depuração para aplicativos COM+ dependem do idioma em que você opta por escrever seu componente.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Depurando aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646491"
---
# <a name="debugging-com-applications"></a><span data-ttu-id="b2c29-103">Depurando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="b2c29-103">Debugging COM+ Applications</span></span>

<span data-ttu-id="b2c29-104">As técnicas de depuração para aplicativos COM+ dependem do idioma em que você opta por escrever seu componente.</span><span class="sxs-lookup"><span data-stu-id="b2c29-104">Debugging techniques for COM+ applications depend on the language in which you choose to write your component.</span></span>

<span data-ttu-id="b2c29-105">Se você codificar em Microsoft Visual C++, poderá iniciar o depurador em C++ ou, com um cliente remoto, poderá depurar usando o controle de procedimento remoto OLE (RPC) e a depuração Just-in-time (JIT).</span><span class="sxs-lookup"><span data-stu-id="b2c29-105">If you code in Microsoft Visual C++, you can launch the debugger in C++ or, with a remote client, you can debug by using OLE remote procedure control (RPC) and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="b2c29-106">Você sempre pode usar a ferramenta administrativa serviços de componentes para depurar seu componente com a configuração COM+ **Iniciar no depurador** na guia **avançado** da caixa de diálogo **Propriedades** do aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="b2c29-106">You can always use the Component Services administrative tool to debug your component with the COM+ **Launch in debugger** setting on the **Advanced** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="b2c29-107">Para obter mais informações sobre os componentes de depuração codificados em C++, consulte [depuração de componentes escritos em Visual C++](debugging-components-written-in-visual-c--.md).</span><span class="sxs-lookup"><span data-stu-id="b2c29-107">For more information on debugging components coded in C++, see [Debugging Components Written in Visual C++](debugging-components-written-in-visual-c--.md).</span></span>

<span data-ttu-id="b2c29-108">A menos que você esteja Depurando no momento vários threads, rastreamento de componentes, chamadas remotas ou isolamento de processo, você pode usar o ambiente de Visual Basic da Microsoft para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="b2c29-108">Unless you are currently debugging multithreading, component tracking, remote calls, or process isolation, you can use the Microsoft Visual Basic environment for debugging purposes.</span></span> <span data-ttu-id="b2c29-109">[Componentes de depuração escritos em Visual Basic](debugging-components-written-in-visual-basic.md) descreve o processo de depuração em um ambiente de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b2c29-109">[Debugging Components Written in Visual Basic](debugging-components-written-in-visual-basic.md) describes the debugging process within a Visual Basic environment.</span></span>

<span data-ttu-id="b2c29-110">O tópico [Depurando no Visual Basic IDE](debugging-in-the-visual-basic-ide.md) fornece uma visão geral com diretrizes, dicas e um procedimento sobre a depuração no IDE (ambiente de desenvolvimento integrado).</span><span class="sxs-lookup"><span data-stu-id="b2c29-110">The topic [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md) provides a general overview with guidelines, tips and a procedure on debugging in the integrated development environment (IDE).</span></span>

<span data-ttu-id="b2c29-111">Para exibir mais informações sobre a depuração de processos avançados, consulte [Depurando componentes Visual Basic compilados](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="b2c29-111">To view more information about debugging advanced processes, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

> [!Note]  
> <span data-ttu-id="b2c29-112">Várias limitações associadas ao uso do ambiente de Visual Basic para depurar componentes com o MTS foram resolvidas para COM+.</span><span class="sxs-lookup"><span data-stu-id="b2c29-112">Several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="b2c29-113">Para obter mais informações, consulte [suporte à depuração de Visual Basic com+ em contraste com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="b2c29-113">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b2c29-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2c29-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2c29-115">Tratamento de erros no COM+</span><span class="sxs-lookup"><span data-stu-id="b2c29-115">Handling Errors in COM+</span></span>](handling-errors-in-com-.md)
</dt> </dl>

 

 



