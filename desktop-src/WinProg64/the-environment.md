---
title: O ambiente
description: Os desenvolvedores que trabalham em aplicativos para o Windows de 64 bits encontrarão o ambiente de desenvolvimento praticamente idêntico ao ambiente de desenvolvimento para o Windows de 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- Programação do ambiente de desenvolvimento de 64 bits do Windows
- Programação de ambiente de 64 bits do Windows
- Guia de programação do Windows de 64 bits, programação do Windows de 64 bits, ambiente de desenvolvimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005187"
---
# <a name="the-environment"></a><span data-ttu-id="c759e-106">O ambiente</span><span class="sxs-lookup"><span data-stu-id="c759e-106">The Environment</span></span>

<span data-ttu-id="c759e-107">Os desenvolvedores que trabalham em aplicativos para o Windows de 64 bits encontrarão o ambiente de desenvolvimento praticamente idêntico ao ambiente de desenvolvimento para o Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c759e-107">Developers working on applications for 64-bit Windows will find the development environment virtually identical to the development environment for 32-bit Windows.</span></span> <span data-ttu-id="c759e-108">As APIs existentes foram modificadas quando necessário para permitir que elas reflitam a precisão da plataforma na qual estão sendo executadas.</span><span class="sxs-lookup"><span data-stu-id="c759e-108">The existing APIs have been modified where necessary to allow them to reflect the precision of the platform on which they are running.</span></span> <span data-ttu-id="c759e-109">O resultado é simplicidade e uma pequena curva de aprendizado para o desenvolvedor — escrever código para o Windows de 64 bits é como escrever código para o Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c759e-109">The result is simplicity and a short learning curve for the developer—writing code for 64-bit Windows is just like writing code for 32-bit Windows.</span></span>

<span data-ttu-id="c759e-110">Os arquivos de cabeçalho do Windows dão suporte a novos tipos de dados que permitem ponteiros e variáveis associadas a ponteiros para refletir a precisão da plataforma.</span><span class="sxs-lookup"><span data-stu-id="c759e-110">The Windows header files support new data types that allow pointers and pointer-associated variables to reflect the precision of the platform.</span></span> <span data-ttu-id="c759e-111">Isso significa que os desenvolvedores podem compilar uma única base de origem para execução nativa em um Windows de 32 bits ou Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c759e-111">This means that developers can compile a single source base to run natively on either 32-bit Windows or 64-bit Windows.</span></span> <span data-ttu-id="c759e-112">Essa estratégia reduz o custo de desenvolvimento de aplicativos que aproveitam o hardware de 64 bits, como processadores AMD Opteron ou Athlon64 ou processadores Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="c759e-112">This strategy reduces the cost of developing applications that leverage 64-bit hardware such as AMD Opteron or Athlon64 processors or Intel Itanium processors.</span></span>

<span data-ttu-id="c759e-113">Você terá mais tempo para tornar seus aplicativos 64-bit prontos se adotar as novas convenções de tipo de dados assim que possível.</span><span class="sxs-lookup"><span data-stu-id="c759e-113">You will have more time to make your applications 64-bit ready if you adopt the new data-type conventions as soon as possible.</span></span> <span data-ttu-id="c759e-114">Se você estiver alterando seu código, deverá alterar as definições de dados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c759e-114">If you are changing your code, you should change the data definitions at the same time.</span></span> <span data-ttu-id="c759e-115">Teste o aplicativo em um Windows de 32 bits, execute-o por meio do compilador de 64 bits (descrito nas [ferramentas](the-tools.md)) e o aplicativo estará pronto para teste quando você tiver o hardware de bits de 64 apropriado.</span><span class="sxs-lookup"><span data-stu-id="c759e-115">Test the application on 32-bit Windows, run it through the 64-bit compiler (described in [The Tools](the-tools.md)), and the application will be ready to test when you have the appropriate 64-bit hardware.</span></span>

 

 




