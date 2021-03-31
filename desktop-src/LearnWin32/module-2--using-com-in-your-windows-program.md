---
title: Usando COM em seu aplicativo do Windows
description: O módulo 1 desta série mostrou como criar uma janela e responder a mensagens de janela como o WM \_ Paint e o WM \_ Close. O módulo 2 apresenta a Component Object Model (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641012"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a><span data-ttu-id="dc158-104">Módulo 2.</span><span class="sxs-lookup"><span data-stu-id="dc158-104">Module 2.</span></span> <span data-ttu-id="dc158-105">Usando COM em seu programa de Windows-Based</span><span class="sxs-lookup"><span data-stu-id="dc158-105">Using COM in Your Windows-Based Program</span></span>

<span data-ttu-id="dc158-106">O [módulo 1](your-first-windows-program.md) desta série mostrou como criar uma janela e responder a mensagens de janela como o [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e o [**WM \_ Close**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="dc158-106">[Module 1](your-first-windows-program.md) of this series showed how to create a window and respond to window messages such as [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span> <span data-ttu-id="dc158-107">O módulo 2 apresenta a Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="dc158-107">Module 2 introduces the Component Object Model (COM).</span></span>

<span data-ttu-id="dc158-108">COM é uma especificação para a criação de componentes de software reutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="dc158-108">COM is a specification for creating reusable software components.</span></span> <span data-ttu-id="dc158-109">Muitos dos recursos que você usará em um programa moderno baseado no Windows contam COM o COM, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dc158-109">Many of the features that you will use in a modern Windows-based program rely on COM, such as the following:</span></span>

-   <span data-ttu-id="dc158-110">Gráficos (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="dc158-110">Graphics (Direct2D)</span></span>
-   <span data-ttu-id="dc158-111">Texto (DirectWrite)</span><span class="sxs-lookup"><span data-stu-id="dc158-111">Text (DirectWrite)</span></span>
-   <span data-ttu-id="dc158-112">O Shell do Windows</span><span class="sxs-lookup"><span data-stu-id="dc158-112">The Windows Shell</span></span>
-   <span data-ttu-id="dc158-113">O controle da faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="dc158-113">The Ribbon control</span></span>
-   <span data-ttu-id="dc158-114">Animação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="dc158-114">UI animation</span></span>

<span data-ttu-id="dc158-115">(Algumas tecnologias nessa lista usam um subconjunto de COM e, portanto, não são "puras" COM.)</span><span class="sxs-lookup"><span data-stu-id="dc158-115">(Some technologies on this list use a subset of COM and are therefore not "pure" COM.)</span></span>

<span data-ttu-id="dc158-116">COM tem uma reputação de ser difícil de aprender.</span><span class="sxs-lookup"><span data-stu-id="dc158-116">COM has a reputation for being difficult to learn.</span></span> <span data-ttu-id="dc158-117">E é verdade que escrever um novo módulo de software para dar suporte a COM pode ser complicado.</span><span class="sxs-lookup"><span data-stu-id="dc158-117">And it is true that writing a new software module to support COM can be tricky.</span></span> <span data-ttu-id="dc158-118">Mas se o seu programa for estritamente um *consumidor* de com, você verá que com é mais fácil entender do que o esperado.</span><span class="sxs-lookup"><span data-stu-id="dc158-118">But if your program is strictly a *consumer* of COM, you may find that COM is easier to understand than you expect.</span></span>

<span data-ttu-id="dc158-119">Este módulo mostra como chamar APIs baseadas em COM em seu programa.</span><span class="sxs-lookup"><span data-stu-id="dc158-119">This module shows how to call COM-based APIs in your program.</span></span> <span data-ttu-id="dc158-120">Ele também descreve algumas das razões por trás do design de COM.</span><span class="sxs-lookup"><span data-stu-id="dc158-120">It also describes some of the reasoning behind the design of COM.</span></span> <span data-ttu-id="dc158-121">Se você entender por que o COM foi projetado como está, poderá programar com ele com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="dc158-121">If you understand why COM is designed as it is, you can program with it more effectively.</span></span> <span data-ttu-id="dc158-122">A segunda parte do módulo descreve algumas práticas de programação recomendadas para COM.</span><span class="sxs-lookup"><span data-stu-id="dc158-122">The second part of the module describes some recommended programming practices for COM.</span></span>

<span data-ttu-id="dc158-123">O COM foi introduzido em 1993 para dar suporte ao OLE (vinculação e inserção de objetos) 2,0.</span><span class="sxs-lookup"><span data-stu-id="dc158-123">COM was introduced in 1993 to support Object Linking and Embedding (OLE) 2.0.</span></span> <span data-ttu-id="dc158-124">Às vezes, as pessoas acham que o COM e o OLE são a mesma coisa.</span><span class="sxs-lookup"><span data-stu-id="dc158-124">People sometimes think that COM and OLE are the same thing.</span></span> <span data-ttu-id="dc158-125">Isso pode ser outro motivo para a percepção de que COM é difícil de aprender.</span><span class="sxs-lookup"><span data-stu-id="dc158-125">This may be another reason for the perception that COM is difficult to learn.</span></span> <span data-ttu-id="dc158-126">O OLE 2,0 foi criado com base em COM, mas você não precisa conhecer OLE para entender COM.</span><span class="sxs-lookup"><span data-stu-id="dc158-126">OLE 2.0 is built on COM, but you do not have to know OLE to understand COM.</span></span>

<span data-ttu-id="dc158-127">COM é um *padrão binário*, não um padrão de idioma: define a interface binária entre um aplicativo e um componente de software.</span><span class="sxs-lookup"><span data-stu-id="dc158-127">COM is a *binary standard*, not a language standard: It defines the binary interface between an application and a software component.</span></span> <span data-ttu-id="dc158-128">Como um padrão binário, o COM é neutro em linguagem, embora seja mapeado naturalmente para determinadas construções de C++.</span><span class="sxs-lookup"><span data-stu-id="dc158-128">As a binary standard, COM is language-neutral, although it maps naturally to certain C++ constructs.</span></span> <span data-ttu-id="dc158-129">Este módulo se concentrará em três grandes metas do COM:</span><span class="sxs-lookup"><span data-stu-id="dc158-129">This module will focus on three major goals of COM:</span></span>

-   <span data-ttu-id="dc158-130">Separar a implementação de um objeto de sua interface.</span><span class="sxs-lookup"><span data-stu-id="dc158-130">Separating the implementation of an object from its interface.</span></span>
-   <span data-ttu-id="dc158-131">Gerenciando o tempo de vida de um objeto.</span><span class="sxs-lookup"><span data-stu-id="dc158-131">Managing the lifetime of an object.</span></span>
-   <span data-ttu-id="dc158-132">Descobrindo os recursos de um objeto em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="dc158-132">Discovering the capabilities of an object at run time.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dc158-133">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="dc158-133">In this section</span></span>

-   [<span data-ttu-id="dc158-134">O que é uma interface COM?</span><span class="sxs-lookup"><span data-stu-id="dc158-134">What Is a COM Interface?</span></span>](what-is-a-com-interface-.md)
-   [<span data-ttu-id="dc158-135">Inicializando a biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="dc158-135">Initializing the COM Library</span></span>](initializing-the-com-library.md)
-   [<span data-ttu-id="dc158-136">Códigos de erro em COM</span><span class="sxs-lookup"><span data-stu-id="dc158-136">Error Codes in COM</span></span>](error-codes-in-com.md)
-   [<span data-ttu-id="dc158-137">Criando um objeto em COM</span><span class="sxs-lookup"><span data-stu-id="dc158-137">Creating an Object in COM</span></span>](creating-an-object-in-com.md)
-   [<span data-ttu-id="dc158-138">Exemplo: a caixa de diálogo abrir</span><span class="sxs-lookup"><span data-stu-id="dc158-138">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)
-   [<span data-ttu-id="dc158-139">Gerenciando o tempo de vida de um objeto</span><span class="sxs-lookup"><span data-stu-id="dc158-139">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)
-   [<span data-ttu-id="dc158-140">Solicitando um objeto para uma interface</span><span class="sxs-lookup"><span data-stu-id="dc158-140">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)
-   [<span data-ttu-id="dc158-141">Alocação de memória em COM</span><span class="sxs-lookup"><span data-stu-id="dc158-141">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)
-   [<span data-ttu-id="dc158-142">Práticas de codificação COM</span><span class="sxs-lookup"><span data-stu-id="dc158-142">COM Coding Practices</span></span>](com-coding-practices.md)
-   [<span data-ttu-id="dc158-143">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="dc158-143">Error Handling in COM</span></span>](error-handling-in-com.md)

## <a name="related-topics"></a><span data-ttu-id="dc158-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc158-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc158-145">Aprenda a programar para Windows em C++</span><span class="sxs-lookup"><span data-stu-id="dc158-145">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 