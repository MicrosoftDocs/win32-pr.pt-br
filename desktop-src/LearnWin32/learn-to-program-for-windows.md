---
title: Introdução ao Win32 e C++
description: O objetivo desta série de introdução é ensinar como escrever um programa de desktop em C++ usando o Win32 e APIs COM.
ms.assetid: a9470cb9-a1e7-4d6d-a4be-61b81d209ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b1ad80530877e9502d158a16295013e3f4a05e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637117"
---
# <a name="get-started-with-win32-and-c"></a><span data-ttu-id="dc18c-103">Introdução ao Win32 e C++</span><span class="sxs-lookup"><span data-stu-id="dc18c-103">Get Started with Win32 and C++</span></span>

<span data-ttu-id="dc18c-104">O objetivo desta série de introdução é ensinar como escrever um programa de desktop em C++ usando o Win32 e APIs COM.</span><span class="sxs-lookup"><span data-stu-id="dc18c-104">The aim of this Get Started series is to teach you how to write a desktop program in C++ using Win32 and COM APIs.</span></span>

<span data-ttu-id="dc18c-105">No primeiro módulo, você aprenderá passo a passo como criar e mostrar uma janela.</span><span class="sxs-lookup"><span data-stu-id="dc18c-105">In the first module, you'll learn step-by-step how to create and show a window.</span></span> <span data-ttu-id="dc18c-106">Os módulos posteriores apresentarão a Component Object Model (COM), os gráficos e o texto e a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc18c-106">Later modules will introduce the Component Object Model (COM), graphics and text, and user input.</span></span>

<span data-ttu-id="dc18c-107">Para esta série, supõe-se que você tenha um bom conhecimento prático da programação em C++.</span><span class="sxs-lookup"><span data-stu-id="dc18c-107">For this series, it is assumed that you have a good working knowledge of C++ programming.</span></span> <span data-ttu-id="dc18c-108">Nenhuma experiência anterior com a programação do Windows é assumida.</span><span class="sxs-lookup"><span data-stu-id="dc18c-108">No previous experience with Windows programming is assumed.</span></span> <span data-ttu-id="dc18c-109">Se você for novo no C++, poderá encontrar material de aprendizagem na [central de desenvolvedores de Visual C++](https://msdn.microsoft.com/vstudio//default.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc18c-109">If you are new to C++, you can find learning material at the [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx).</span></span> <span data-ttu-id="dc18c-110">(Esse recurso pode não estar disponível em alguns idiomas e países.)</span><span class="sxs-lookup"><span data-stu-id="dc18c-110">(This resource may not be available in some languages and countries.)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dc18c-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="dc18c-111">In this section</span></span>



| <span data-ttu-id="dc18c-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="dc18c-112">Topic</span></span>                                                                                                     | <span data-ttu-id="dc18c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc18c-113">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc18c-114">Introdução à programação do Windows em C++</span><span class="sxs-lookup"><span data-stu-id="dc18c-114">Introduction to Windows Programming in C++</span></span>](introduction-to-windows-programming-in-c--.md)<br/>   | <span data-ttu-id="dc18c-115">Esta seção descreve algumas das convenções básicas de terminologia e codificação usadas na programação do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc18c-115">This section describes some of the basic terminology and coding conventions used in Windows programming.</span></span><br/>  |
| [<span data-ttu-id="dc18c-116">Módulo 1. Seu primeiro programa do Windows</span><span class="sxs-lookup"><span data-stu-id="dc18c-116">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)<br/>                         | <span data-ttu-id="dc18c-117">Neste módulo, você criará um programa simples do Windows que mostra uma janela em branco.</span><span class="sxs-lookup"><span data-stu-id="dc18c-117">In this module, you will create a simple Windows program that shows a blank window.</span></span><br/>                       |
| [<span data-ttu-id="dc18c-118">Módulo 2. Usando COM em seu programa do Windows</span><span class="sxs-lookup"><span data-stu-id="dc18c-118">Module 2. Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)<br/> | <span data-ttu-id="dc18c-119">Esse módulo apresenta a Component Object Model (COM), que se baseia em muitas das APIs modernas do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc18c-119">This module introduces the Component Object Model (COM), which underlies many of the modern Windows APIs.</span></span><br/> |
| [<span data-ttu-id="dc18c-120">Módulo 3. Gráficos do Windows</span><span class="sxs-lookup"><span data-stu-id="dc18c-120">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)<br/>                                  | <span data-ttu-id="dc18c-121">Este módulo apresenta a arquitetura de gráficos do Windows, com foco em Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dc18c-121">This module introduces the Windows graphics architecture, with a focus on Direct2D.</span></span><br/>                       |
| [<span data-ttu-id="dc18c-122">Módulo 4. Entrada do usuário</span><span class="sxs-lookup"><span data-stu-id="dc18c-122">Module 4. User Input</span></span>](module-4--user-input.md)<br/>                                               | <span data-ttu-id="dc18c-123">Este módulo descreve a entrada do mouse e do teclado.</span><span class="sxs-lookup"><span data-stu-id="dc18c-123">This module describes mouse and keyboard input.</span></span><br/>                                                           |
| [<span data-ttu-id="dc18c-124">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="dc18c-124">Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)<br/>                                   | <span data-ttu-id="dc18c-125">Contém links para baixar o código de exemplo para esta série.</span><span class="sxs-lookup"><span data-stu-id="dc18c-125">Contains links to download the sample code for this series.</span></span><br/>                                               |



 

 

 





