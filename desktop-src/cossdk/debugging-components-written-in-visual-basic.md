---
description: Componentes de depuração escritos em Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Componentes de depuração escritos em Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773027"
---
# <a name="debugging-components-written-in-visual-basic"></a><span data-ttu-id="da3af-103">Componentes de depuração escritos em Visual Basic</span><span class="sxs-lookup"><span data-stu-id="da3af-103">Debugging Components Written in Visual Basic</span></span>

<span data-ttu-id="da3af-104">Você pode usar o ambiente de desenvolvimento Microsoft Visual Basic 6,0 para depuração em determinados cenários.</span><span class="sxs-lookup"><span data-stu-id="da3af-104">You can use the Microsoft Visual Basic 6.0 development environment for debugging within certain scenarios.</span></span> <span data-ttu-id="da3af-105">O uso de Visual Basic para depuração permite o acesso a ferramentas familiares para Visual Basic programadores.</span><span class="sxs-lookup"><span data-stu-id="da3af-105">Using Visual Basic for debugging allows access to tools familiar to Visual Basic programmers.</span></span> <span data-ttu-id="da3af-106">Por outro lado, como durante a depuração Visual Basic os componentes são executados dentro do processo do ambiente de Visual Basic, pode ser necessário depurar seu componente depois que ele tiver sido compilado usando o ambiente de desenvolvimento do Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="da3af-106">On the other hand, because during debugging Visual Basic components run within the Visual Basic environment's process, it may be necessary to debug your component after it has been compiled by using the Microsoft Visual C++ development environment.</span></span>

<span data-ttu-id="da3af-107">Para obter mais informações sobre a depuração dentro do Visual Basic IDE (ambiente de desenvolvimento integrado), consulte [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span><span class="sxs-lookup"><span data-stu-id="da3af-107">For more information about debugging within the Visual Basic integrated development environment (IDE), see [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span></span> <span data-ttu-id="da3af-108">Para saber mais sobre como depurar Visual Basic componentes depois que eles forem compilados usando o ambiente de desenvolvimento de Visual C++, consulte [Depurando componentes de Visual Basic compilados](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="da3af-108">For more on debugging Visual Basic components after they're compiled using the Visual C++ development environment, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

<span data-ttu-id="da3af-109">Além disso, várias limitações associadas ao uso do ambiente de Visual Basic para depurar componentes com o MTS foram resolvidas para COM+.</span><span class="sxs-lookup"><span data-stu-id="da3af-109">Also, several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="da3af-110">Para obter mais informações, consulte [suporte à depuração de Visual Basic com+ em contraste com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="da3af-110">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

> [!Note]  
> <span data-ttu-id="da3af-111">Se você já tiver usado Visual Basic no mesmo computador que o COM+, talvez tenha notado o suplemento serviços de componentes disponível no ambiente de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="da3af-111">If you have already used Visual Basic on the same computer as COM+, you may have noticed the Component Services add-in available in the Visual Basic environment.</span></span> <span data-ttu-id="da3af-112">Originalmente no MTS, esse recurso foi projetado para atualizar o registro cada vez que você recompilou um componente em um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="da3af-112">Originally in MTS, this feature was designed to update the registry each time you recompiled a component in a COM+ application.</span></span> <span data-ttu-id="da3af-113">No entanto, considerando a natureza da interação do registro do Microsoft Windows e do banco de dados de registro do COM+, algumas configurações podem não ser completamente atualizadas.</span><span class="sxs-lookup"><span data-stu-id="da3af-113">However, given the nature of the interaction of the Microsoft Windows Registry and the COM+ registration database, some settings may not be completely updated.</span></span> <span data-ttu-id="da3af-114">Portanto, em vez de usar os comandos disponíveis com esse suplemento, você deve remover e reinstalar os componentes para atualizar as configurações após a recompilação.</span><span class="sxs-lookup"><span data-stu-id="da3af-114">Therefore, instead of using the commands available with this add-in, you should remove and reinstall your components to update settings after recompiling.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da3af-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da3af-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da3af-116">Componentes de depuração escritos em Visual C++</span><span class="sxs-lookup"><span data-stu-id="da3af-116">Debugging Components Written in Visual C++</span></span>](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



