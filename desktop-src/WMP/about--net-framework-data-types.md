---
title: Sobre tipos de dados de .NET Framework
description: Sobre tipos de dados de .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player,. NET Framework
- Modelo de objeto do Windows Media Player,. NET Framework
- modelo de objeto,. NET Framework
- Windows Media Player Mobile, .NET Framework
- Controle ActiveX do Windows Media Player, .NET Framework
- Controle ActiveX móvel do Windows Media Player, .NET Framework
- Controle ActiveX, .NET Framework
- .NET Framework, tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006018"
---
# <a name="about-net-framework-data-types"></a><span data-ttu-id="c6326-111">Sobre tipos de dados de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="c6326-111">About .NET Framework Data Types</span></span>

<span data-ttu-id="c6326-112">Esta seção contém as informações necessárias para converter a referência de modelo de objeto orientado a script em tipos de dados base do Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c6326-112">This section contains the information you need to translate the script-oriented Object Model Reference into Microsoft .NET Framework base data types.</span></span> <span data-ttu-id="c6326-113">A referência de script do Windows Media Player tem quase todas as informações de que você precisa para usar o controle do Windows Media Player em um programa baseado em .NET Framework e, na maioria dos casos, a sintaxe será semelhante à de outras linguagens de script, como o Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="c6326-113">The Windows Media Player script reference has almost all the information you need to use the Windows Media Player control in a .NET Framework-based program, and in most cases, the syntax will be similar to that of other scripting languages such as Microsoft JScript.</span></span>

<span data-ttu-id="c6326-114">A referência do Windows Media Player fornece o tipo de dados JScript e, se necessário, a conversão de C++.</span><span class="sxs-lookup"><span data-stu-id="c6326-114">The Windows Media Player reference provides the JScript data type and, if necessary, the C++ conversion.</span></span> <span data-ttu-id="c6326-115">Por exemplo, um **número** pode ser retornado por um método.</span><span class="sxs-lookup"><span data-stu-id="c6326-115">For example, a **Number** might be returned by a method.</span></span> <span data-ttu-id="c6326-116">O JScript trata todos os números da mesma forma, mas outras linguagens distinguem entre diferentes tipos de números (inteiro, ponto flutuante e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c6326-116">JScript treats all numbers in the same way, but other languages distinguish between different types of numbers (integer, floating point, and so on).</span></span> <span data-ttu-id="c6326-117">A referência fornece a conversão de C++ para tipos de dados de número porque os números podem ser processados de forma diferente pelo C++.</span><span class="sxs-lookup"><span data-stu-id="c6326-117">The reference gives the C++ conversion for number data types because numbers can be processed differently by C++.</span></span> <span data-ttu-id="c6326-118">Por exemplo, C++ usa o tipo de dados **int** para inteiro aritmético e **flutuante** para ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="c6326-118">For example, C++ uses the **int** data type for integer arithmetic and **float** for floating point.</span></span>

<span data-ttu-id="c6326-119">O .NET Framework usa um sistema um pouco diferente de tipos de dados base.</span><span class="sxs-lookup"><span data-stu-id="c6326-119">The .NET Framework uses a slightly different system of base data types.</span></span> <span data-ttu-id="c6326-120">A tabela a seguir mostra as diferenças nos tipos de dados comuns que você provavelmente usará.</span><span class="sxs-lookup"><span data-stu-id="c6326-120">The following table shows the differences in the common data types you are likely to use.</span></span> <span data-ttu-id="c6326-121">Para obter mais informações sobre .NET Framework tipos de dados básicos e a conversão em outros sistemas de tipo de dados, consulte a discussão guia do desenvolvedor de .NET Framework do namespace System base de tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="c6326-121">For more information on .NET Framework base data types and the conversion to other data type systems, see the .NET Framework Developer's Guide discussion of System Namespace base data types.</span></span>

<span data-ttu-id="c6326-122">Esta tabela fornece o .NET Framework nome da classe e o tipo de dados C#.</span><span class="sxs-lookup"><span data-stu-id="c6326-122">This table gives the .NET Framework class name and the C# data type.</span></span> <span data-ttu-id="c6326-123">Os tipos de dados para outros idiomas são definidos para cada idioma em suas respectivas referências de idioma.</span><span class="sxs-lookup"><span data-stu-id="c6326-123">Data types for other languages are defined for each language in their respective language references.</span></span>



| <span data-ttu-id="c6326-124">Tipo de dados script</span><span class="sxs-lookup"><span data-stu-id="c6326-124">Script data type</span></span> | <span data-ttu-id="c6326-125">Tipo de dados em C++</span><span class="sxs-lookup"><span data-stu-id="c6326-125">C++ data type</span></span>     | <span data-ttu-id="c6326-126">Classe .NET Framework (tipo de dados C#)</span><span class="sxs-lookup"><span data-stu-id="c6326-126">.NET Framework class (C# data type )</span></span> |
|------------------|-------------------|---------------------------------------|
| <span data-ttu-id="c6326-127">**Número**</span><span class="sxs-lookup"><span data-stu-id="c6326-127">**Number**</span></span>       | <span data-ttu-id="c6326-128">**int**</span><span class="sxs-lookup"><span data-stu-id="c6326-128">**int**</span></span>           | <span data-ttu-id="c6326-129">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="c6326-129">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="c6326-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="c6326-130">**Number**</span></span>       | <span data-ttu-id="c6326-131">**longo**</span><span class="sxs-lookup"><span data-stu-id="c6326-131">**long**</span></span>          | <span data-ttu-id="c6326-132">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="c6326-132">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="c6326-133">**Número**</span><span class="sxs-lookup"><span data-stu-id="c6326-133">**Number**</span></span>       | <span data-ttu-id="c6326-134">**double**</span><span class="sxs-lookup"><span data-stu-id="c6326-134">**double**</span></span>        | <span data-ttu-id="c6326-135">**Double** (**duplo**)</span><span class="sxs-lookup"><span data-stu-id="c6326-135">**Double** (**double**)</span></span>               |
| <span data-ttu-id="c6326-136">**Número**</span><span class="sxs-lookup"><span data-stu-id="c6326-136">**Number**</span></span>       | <span data-ttu-id="c6326-137">**float**</span><span class="sxs-lookup"><span data-stu-id="c6326-137">**float**</span></span>         | <span data-ttu-id="c6326-138">**Single** (**float**)</span><span class="sxs-lookup"><span data-stu-id="c6326-138">**Single** (**float**)</span></span>                |
| <span data-ttu-id="c6326-139">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c6326-139">**String**</span></span>       | <span data-ttu-id="c6326-140">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="c6326-140">**BSTR**</span></span>          | <span data-ttu-id="c6326-141">**Cadeia de caracteres** (**cadeia de caracteres**)</span><span class="sxs-lookup"><span data-stu-id="c6326-141">**String** (**string**)</span></span>               |
| <span data-ttu-id="c6326-142">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="c6326-142">**Boolean**</span></span>      | <span data-ttu-id="c6326-143">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="c6326-143">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c6326-144">**Booliano** (**bool**)</span><span class="sxs-lookup"><span data-stu-id="c6326-144">**Boolean** (**bool**)</span></span>                |
| <span data-ttu-id="c6326-145">**Objeto**</span><span class="sxs-lookup"><span data-stu-id="c6326-145">**Object**</span></span>       | <span data-ttu-id="c6326-146">**Objeto**</span><span class="sxs-lookup"><span data-stu-id="c6326-146">**Object**</span></span>        | <span data-ttu-id="c6326-147">**Objeto** (**objeto**)</span><span class="sxs-lookup"><span data-stu-id="c6326-147">**Object** (**object**)</span></span>               |



 

<span data-ttu-id="c6326-148">Se você estiver usando o Visual Studio, poderá usar a tecnologia Microsoft IntelliSense para determinar qual tipo de dados é esperado para uma função específica.</span><span class="sxs-lookup"><span data-stu-id="c6326-148">If you are using Visual Studio, you can use the Microsoft IntelliSense technology to determine what data type is expected for a specific function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6326-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6326-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6326-150">**Inserindo o controle do Windows Media Player em uma solução .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="c6326-150">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="c6326-151">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="c6326-151">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




