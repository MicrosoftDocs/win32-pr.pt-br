---
title: Diretivas de pré-processador (menus e outros recursos)
description: Você pode usar as diretivas descritas na tabela a seguir, conforme necessário no script de recurso. Eles instruem o RC para executar ações ou para atribuir valores a nomes.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilador de recurso, diretivas de pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294732"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a><span data-ttu-id="b56e5-105">Diretivas de pré-processador (menus e outros recursos)</span><span class="sxs-lookup"><span data-stu-id="b56e5-105">Preprocessor Directives (Menus and Other Resources)</span></span>

<span data-ttu-id="b56e5-106">Você pode usar as diretivas descritas na tabela a seguir, conforme necessário no script de recurso.</span><span class="sxs-lookup"><span data-stu-id="b56e5-106">You can use the directives described in the following table as needed in your resource script.</span></span> <span data-ttu-id="b56e5-107">Eles instruem o RC para executar ações ou para atribuir valores a nomes.</span><span class="sxs-lookup"><span data-stu-id="b56e5-107">They instruct RC to perform actions or to assign values to names.</span></span>



| <span data-ttu-id="b56e5-108">Diretiva</span><span class="sxs-lookup"><span data-stu-id="b56e5-108">Directive</span></span>                     | <span data-ttu-id="b56e5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b56e5-109">Description</span></span>                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b56e5-110">**\#definir**</span><span class="sxs-lookup"><span data-stu-id="b56e5-110">**\#define**</span></span>](-define.md)   | <span data-ttu-id="b56e5-111">Define um nome especificado atribuindo a ele um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="b56e5-111">Defines a specified name by assigning it a given value.</span></span>               |
| [<span data-ttu-id="b56e5-112">**\#elif**</span><span class="sxs-lookup"><span data-stu-id="b56e5-112">**\#elif**</span></span>](-elif.md)       | <span data-ttu-id="b56e5-113">Marca uma cláusula opcional de um bloco de compilação condicional.</span><span class="sxs-lookup"><span data-stu-id="b56e5-113">Marks an optional clause of a conditional-compilation block.</span></span>          |
| [<span data-ttu-id="b56e5-114">**\#else**</span><span class="sxs-lookup"><span data-stu-id="b56e5-114">**\#else**</span></span>](-else.md)       | <span data-ttu-id="b56e5-115">Marca a última cláusula opcional de um bloco de compilação condicional.</span><span class="sxs-lookup"><span data-stu-id="b56e5-115">Marks the last optional clause of a conditional-compilation block.</span></span>    |
| [<span data-ttu-id="b56e5-116">**\#endif**</span><span class="sxs-lookup"><span data-stu-id="b56e5-116">**\#endif**</span></span>](-endif.md)     | <span data-ttu-id="b56e5-117">Marca o final de um bloco de compilação condicional.</span><span class="sxs-lookup"><span data-stu-id="b56e5-117">Marks the end of a conditional-compilation block.</span></span>                     |
| [<span data-ttu-id="b56e5-118">**\#que**</span><span class="sxs-lookup"><span data-stu-id="b56e5-118">**\#if**</span></span>](-if.md)           | <span data-ttu-id="b56e5-119">Compila condicionalmente o script se uma expressão especificada for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="b56e5-119">Conditionally compiles the script if a specified expression is true.</span></span>  |
| [<span data-ttu-id="b56e5-120">**\#ifdef**</span><span class="sxs-lookup"><span data-stu-id="b56e5-120">**\#ifdef**</span></span>](-ifdef.md)     | <span data-ttu-id="b56e5-121">Compila condicionalmente o script se um nome especificado for definido.</span><span class="sxs-lookup"><span data-stu-id="b56e5-121">Conditionally compiles the script if a specified name is defined.</span></span>     |
| [<span data-ttu-id="b56e5-122">**\#ifndef**</span><span class="sxs-lookup"><span data-stu-id="b56e5-122">**\#ifndef**</span></span>](-ifndef.md)   | <span data-ttu-id="b56e5-123">Compila condicionalmente o script se um nome especificado não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="b56e5-123">Conditionally compiles the script if a specified name is not defined.</span></span> |
| [<span data-ttu-id="b56e5-124">**\#incluir**</span><span class="sxs-lookup"><span data-stu-id="b56e5-124">**\#include**</span></span>](-include.md) | <span data-ttu-id="b56e5-125">Copia o conteúdo de um arquivo para o arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="b56e5-125">Copies the contents of a file into the resource-definition file.</span></span>      |
| [<span data-ttu-id="b56e5-126">**\#undef**</span><span class="sxs-lookup"><span data-stu-id="b56e5-126">**\#undef**</span></span>](-undef.md)     | <span data-ttu-id="b56e5-127">Remove a definição do nome especificado.</span><span class="sxs-lookup"><span data-stu-id="b56e5-127">Removes the definition of the specified name.</span></span>                         |



 

<span data-ttu-id="b56e5-128">Para definir símbolos para seus identificadores de recursos, use a diretiva **\# definir** para defini-los em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b56e5-128">To define symbols for your resource identifiers, use the **\#define** directive to define them in a header file.</span></span> <span data-ttu-id="b56e5-129">Inclua esse cabeçalho no script de recurso e no código-fonte do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b56e5-129">Include this header both in the resource script and your application source code.</span></span> <span data-ttu-id="b56e5-130">Da mesma forma, você define os valores para atributos de recurso e estilos, incluindo o Windows. h no script de recurso.</span><span class="sxs-lookup"><span data-stu-id="b56e5-130">Similarly, you define the values for resource attributes and styles by including Windows.h in the resource script.</span></span>

<span data-ttu-id="b56e5-131">O RC trata os arquivos com as extensões. c e. h de maneira especial.</span><span class="sxs-lookup"><span data-stu-id="b56e5-131">RC treats files with the .c and .h extensions in a special manner.</span></span> <span data-ttu-id="b56e5-132">Ele pressupõe que um arquivo com uma dessas extensões não contém recursos.</span><span class="sxs-lookup"><span data-stu-id="b56e5-132">It assumes that a file with one of these extensions does not contain resources.</span></span> <span data-ttu-id="b56e5-133">Se um arquivo tiver a extensão de nome de arquivo. c ou. h, o RC ignorará todas as linhas no arquivo, exceto as diretivas de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="b56e5-133">If a file has the .c or .h file name extension, RC ignores all lines in the file except the preprocessor directives.</span></span> <span data-ttu-id="b56e5-134">Portanto, para incluir um arquivo que contém recursos em outro script de recurso, dê ao arquivo uma extensão diferente de. c ou. h.</span><span class="sxs-lookup"><span data-stu-id="b56e5-134">Therefore, to include a file that contains resources in another resource script, give the file to be included an extension other than .c or .h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b56e5-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b56e5-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b56e5-136">Diretivas pragma</span><span class="sxs-lookup"><span data-stu-id="b56e5-136">Pragma Directives</span></span>](pragma-directives.md)
</dt> </dl>

 

 




