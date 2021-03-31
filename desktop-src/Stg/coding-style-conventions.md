---
title: Convenções de estilo de codificação
description: As convenções de estilo de codificação são usadas nesta série de exemplo para auxiliar na clareza e na consistência.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103643015"
---
# <a name="coding-style-conventions"></a><span data-ttu-id="b2149-103">Convenções de estilo de codificação</span><span class="sxs-lookup"><span data-stu-id="b2149-103">Coding Style Conventions</span></span>

<span data-ttu-id="b2149-104">As convenções de estilo de codificação são usadas nesta série de exemplo para auxiliar na clareza e na consistência.</span><span class="sxs-lookup"><span data-stu-id="b2149-104">Coding style conventions are used in this sample series to aid clarity and consistency.</span></span> <span data-ttu-id="b2149-105">As convenções de notação "húngaro" são usadas.</span><span class="sxs-lookup"><span data-stu-id="b2149-105">The "Hungarian" notation conventions are used.</span></span> <span data-ttu-id="b2149-106">Elas se tornaram uma prática de codificação comum na programação do Win32.</span><span class="sxs-lookup"><span data-stu-id="b2149-106">These have become a common coding practice in Win32 programming.</span></span> <span data-ttu-id="b2149-107">Eles incluem notações de prefixo variável que fornecem a nomes de variáveis uma sugestão do tipo da variável.</span><span class="sxs-lookup"><span data-stu-id="b2149-107">They include variable prefix notations that give to variable names a suggestion of the type of the variable.</span></span>

<span data-ttu-id="b2149-108">A tabela a seguir lista os prefixos comuns.</span><span class="sxs-lookup"><span data-stu-id="b2149-108">The following table lists common prefixes.</span></span>



| <span data-ttu-id="b2149-109">Prefixo</span><span class="sxs-lookup"><span data-stu-id="b2149-109">Prefix</span></span> | <span data-ttu-id="b2149-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2149-110">Description</span></span>                         |
|--------|-------------------------------------|
| <span data-ttu-id="b2149-111">um</span><span class="sxs-lookup"><span data-stu-id="b2149-111">a</span></span>      | <span data-ttu-id="b2149-112">Array</span><span class="sxs-lookup"><span data-stu-id="b2149-112">Array</span></span>                               |
| <span data-ttu-id="b2149-113">b</span><span class="sxs-lookup"><span data-stu-id="b2149-113">b</span></span>      | <span data-ttu-id="b2149-114">BOOL (int)</span><span class="sxs-lookup"><span data-stu-id="b2149-114">BOOL (int)</span></span>                          |
| <span data-ttu-id="b2149-115">c</span><span class="sxs-lookup"><span data-stu-id="b2149-115">c</span></span>      | <span data-ttu-id="b2149-116">Char</span><span class="sxs-lookup"><span data-stu-id="b2149-116">Char</span></span>                                |
| <span data-ttu-id="b2149-117">CB</span><span class="sxs-lookup"><span data-stu-id="b2149-117">cb</span></span>     | <span data-ttu-id="b2149-118">Contagem de bytes</span><span class="sxs-lookup"><span data-stu-id="b2149-118">Count of bytes</span></span>                      |
| <span data-ttu-id="b2149-119">CD</span><span class="sxs-lookup"><span data-stu-id="b2149-119">cr</span></span>     | <span data-ttu-id="b2149-120">Valor de referência de cor</span><span class="sxs-lookup"><span data-stu-id="b2149-120">Color reference value</span></span>               |
| <span data-ttu-id="b2149-121">CX</span><span class="sxs-lookup"><span data-stu-id="b2149-121">cx</span></span>     | <span data-ttu-id="b2149-122">Contagem de x (curta)</span><span class="sxs-lookup"><span data-stu-id="b2149-122">Count of x (short)</span></span>                  |
| <span data-ttu-id="b2149-123">dw</span><span class="sxs-lookup"><span data-stu-id="b2149-123">dw</span></span>     | <span data-ttu-id="b2149-124">DWORD (longo sem sinal)</span><span class="sxs-lookup"><span data-stu-id="b2149-124">DWORD (unsigned long)</span></span>               |
| <span data-ttu-id="b2149-125">f</span><span class="sxs-lookup"><span data-stu-id="b2149-125">f</span></span>      | <span data-ttu-id="b2149-126">Flags (geralmente valores de vários bits)</span><span class="sxs-lookup"><span data-stu-id="b2149-126">Flags (usually multiple bit values)</span></span> |
| <span data-ttu-id="b2149-127">fn</span><span class="sxs-lookup"><span data-stu-id="b2149-127">fn</span></span>     | <span data-ttu-id="b2149-128">Função</span><span class="sxs-lookup"><span data-stu-id="b2149-128">Function</span></span>                            |
| <span data-ttu-id="b2149-129">m\_</span><span class="sxs-lookup"><span data-stu-id="b2149-129">g\_</span></span>    | <span data-ttu-id="b2149-130">Global</span><span class="sxs-lookup"><span data-stu-id="b2149-130">Global</span></span>                              |
| <span data-ttu-id="b2149-131">h</span><span class="sxs-lookup"><span data-stu-id="b2149-131">h</span></span>      | <span data-ttu-id="b2149-132">Handle</span><span class="sxs-lookup"><span data-stu-id="b2149-132">Handle</span></span>                              |
| <span data-ttu-id="b2149-133">i</span><span class="sxs-lookup"><span data-stu-id="b2149-133">i</span></span>      | <span data-ttu-id="b2149-134">Inteiro</span><span class="sxs-lookup"><span data-stu-id="b2149-134">Integer</span></span>                             |
| <span data-ttu-id="b2149-135">l</span><span class="sxs-lookup"><span data-stu-id="b2149-135">l</span></span>      | <span data-ttu-id="b2149-136">long</span><span class="sxs-lookup"><span data-stu-id="b2149-136">Long</span></span>                                |
| <span data-ttu-id="b2149-137">lp</span><span class="sxs-lookup"><span data-stu-id="b2149-137">lp</span></span>     | <span data-ttu-id="b2149-138">Ponteiro longo</span><span class="sxs-lookup"><span data-stu-id="b2149-138">Long pointer</span></span>                        |
| <span data-ttu-id="b2149-139">d\_</span><span class="sxs-lookup"><span data-stu-id="b2149-139">m\_</span></span>    | <span data-ttu-id="b2149-140">Membro de dados de uma classe</span><span class="sxs-lookup"><span data-stu-id="b2149-140">Data member of a class</span></span>              |
| <span data-ttu-id="b2149-141">n</span><span class="sxs-lookup"><span data-stu-id="b2149-141">n</span></span>      | <span data-ttu-id="b2149-142">Int curta</span><span class="sxs-lookup"><span data-stu-id="b2149-142">Short int</span></span>                           |
| <span data-ttu-id="b2149-143">p</span><span class="sxs-lookup"><span data-stu-id="b2149-143">p</span></span>      | <span data-ttu-id="b2149-144">Ponteiro</span><span class="sxs-lookup"><span data-stu-id="b2149-144">Pointer</span></span>                             |
| <span data-ttu-id="b2149-145">s</span><span class="sxs-lookup"><span data-stu-id="b2149-145">s</span></span>      | <span data-ttu-id="b2149-146">String</span><span class="sxs-lookup"><span data-stu-id="b2149-146">String</span></span>                              |
| <span data-ttu-id="b2149-147">sz</span><span class="sxs-lookup"><span data-stu-id="b2149-147">sz</span></span>     | <span data-ttu-id="b2149-148">Cadeia de caracteres terminada em zero</span><span class="sxs-lookup"><span data-stu-id="b2149-148">Zero terminated String</span></span>              |
| <span data-ttu-id="b2149-149">tm</span><span class="sxs-lookup"><span data-stu-id="b2149-149">tm</span></span>     | <span data-ttu-id="b2149-150">Métrica de texto</span><span class="sxs-lookup"><span data-stu-id="b2149-150">Text metric</span></span>                         |
| <span data-ttu-id="b2149-151">u</span><span class="sxs-lookup"><span data-stu-id="b2149-151">u</span></span>      | <span data-ttu-id="b2149-152">Int não assinado</span><span class="sxs-lookup"><span data-stu-id="b2149-152">Unsigned int</span></span>                        |
| <span data-ttu-id="b2149-153">UL</span><span class="sxs-lookup"><span data-stu-id="b2149-153">ul</span></span>     | <span data-ttu-id="b2149-154">Longo não atribuído (ULONG)</span><span class="sxs-lookup"><span data-stu-id="b2149-154">Unsigned long (ULONG)</span></span>               |
| <span data-ttu-id="b2149-155">w</span><span class="sxs-lookup"><span data-stu-id="b2149-155">w</span></span>      | <span data-ttu-id="b2149-156">PALAVRA (sem sinal curto)</span><span class="sxs-lookup"><span data-stu-id="b2149-156">WORD (unsigned short)</span></span>               |
| <span data-ttu-id="b2149-157">x, y</span><span class="sxs-lookup"><span data-stu-id="b2149-157">x,y</span></span>    | <span data-ttu-id="b2149-158">coordenadas x, y (abreviadas)</span><span class="sxs-lookup"><span data-stu-id="b2149-158">x, y coordinates (short)</span></span>            |



 

<span data-ttu-id="b2149-159">Essas muitas vezes são combinadas, como no seguinte.</span><span class="sxs-lookup"><span data-stu-id="b2149-159">These are often combined, as in the following.</span></span>



| <span data-ttu-id="b2149-160">Combinação de prefixo</span><span class="sxs-lookup"><span data-stu-id="b2149-160">Prefix combination</span></span> | <span data-ttu-id="b2149-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2149-161">Description</span></span>                                             |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="b2149-162">pszMyString</span><span class="sxs-lookup"><span data-stu-id="b2149-162">pszMyString</span></span>        | <span data-ttu-id="b2149-163">Um ponteiro para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b2149-163">A pointer to a string.</span></span>                                  |
| <span data-ttu-id="b2149-164">\_pszMyString m</span><span class="sxs-lookup"><span data-stu-id="b2149-164">m\_pszMyString</span></span>     | <span data-ttu-id="b2149-165">Um ponteiro para uma cadeia de caracteres que é um membro de dados de uma classe.</span><span class="sxs-lookup"><span data-stu-id="b2149-165">A pointer to a string that is a data member of a class.</span></span> |



 

<span data-ttu-id="b2149-166">Outras convenções são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b2149-166">Other conventions are listed in the following table.</span></span>



| <span data-ttu-id="b2149-167">Convenção</span><span class="sxs-lookup"><span data-stu-id="b2149-167">Convention</span></span>       | <span data-ttu-id="b2149-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2149-168">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="b2149-169">CMyClass</span><span class="sxs-lookup"><span data-stu-id="b2149-169">CMyClass</span></span>         | <span data-ttu-id="b2149-170">Prefixo ' C' para nomes de classe C++.</span><span class="sxs-lookup"><span data-stu-id="b2149-170">Prefix 'C' for C++ class names.</span></span>                          |
| <span data-ttu-id="b2149-171">COMyObjectClass</span><span class="sxs-lookup"><span data-stu-id="b2149-171">COMyObjectClass</span></span>  | <span data-ttu-id="b2149-172">Prefixo ' CO ' para nomes de classe de objeto COM.</span><span class="sxs-lookup"><span data-stu-id="b2149-172">Prefix 'CO' for COM object class names.</span></span>                  |
| <span data-ttu-id="b2149-173">CFMyClassFactory</span><span class="sxs-lookup"><span data-stu-id="b2149-173">CFMyClassFactory</span></span> | <span data-ttu-id="b2149-174">Prefixo ' CF ' para nomes de fábrica de classes COM.</span><span class="sxs-lookup"><span data-stu-id="b2149-174">Prefix 'CF' for COM class factory names.</span></span>                 |
| <span data-ttu-id="b2149-175">IMinhaInterface</span><span class="sxs-lookup"><span data-stu-id="b2149-175">IMyInterface</span></span>     | <span data-ttu-id="b2149-176">Prefixo ' I ' para nomes de classe de interface COM.</span><span class="sxs-lookup"><span data-stu-id="b2149-176">Prefix 'I' for COM interface class names.</span></span>                |
| <span data-ttu-id="b2149-177">CImpIMyInterface</span><span class="sxs-lookup"><span data-stu-id="b2149-177">CImpIMyInterface</span></span> | <span data-ttu-id="b2149-178">Prefixo ' CImpI ' para classes de implementação de interface COM.</span><span class="sxs-lookup"><span data-stu-id="b2149-178">Prefix 'CImpI' for COM interface implementation classes.</span></span> |



 

<span data-ttu-id="b2149-179">Algumas convenções consistentes para blocos de cabeçalho de comentário são usadas nesta série de exemplo da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b2149-179">Some consistent conventions for comment header blocks are used in this sample series as follows.</span></span>

## <a name="file-header"></a><span data-ttu-id="b2149-180">Cabeçalho do arquivo</span><span class="sxs-lookup"><span data-stu-id="b2149-180">File Header</span></span>

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a><span data-ttu-id="b2149-181">Bloco de comentário simples</span><span class="sxs-lookup"><span data-stu-id="b2149-181">Plain Comment Block</span></span>

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a><span data-ttu-id="b2149-182">Cabeçalho de declaração de classe</span><span class="sxs-lookup"><span data-stu-id="b2149-182">Class Declaration Header</span></span>

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a><span data-ttu-id="b2149-183">Cabeçalho de definição do método de classe</span><span class="sxs-lookup"><span data-stu-id="b2149-183">Class Method Definition Header</span></span>

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a><span data-ttu-id="b2149-184">Função local ou não exportada</span><span class="sxs-lookup"><span data-stu-id="b2149-184">Unexported or Local Function</span></span>

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a><span data-ttu-id="b2149-185">Cabeçalho de definição de função exportada</span><span class="sxs-lookup"><span data-stu-id="b2149-185">Exported Function Definition Header</span></span>

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a><span data-ttu-id="b2149-186">Cabeçalho de declaração da interface COM</span><span class="sxs-lookup"><span data-stu-id="b2149-186">COM Interface Declaration Header</span></span>

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a><span data-ttu-id="b2149-187">Cabeçalho de declaração de classe de objeto COM</span><span class="sxs-lookup"><span data-stu-id="b2149-187">COM Object Class Declaration Header</span></span>

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

<span data-ttu-id="b2149-188">Todas essas convenções de bloco de comentário têm cadeias de caracteres de token de início e término consistentes.</span><span class="sxs-lookup"><span data-stu-id="b2149-188">All of these comment block conventions have consistent beginning and ending token strings.</span></span> <span data-ttu-id="b2149-189">Essa consistência dá suporte ao processamento automático dos cabeçalhos de alguma maneira.</span><span class="sxs-lookup"><span data-stu-id="b2149-189">This consistency supports automatic processing of the headers in some fashion.</span></span> <span data-ttu-id="b2149-190">Por exemplo, os scripts AWK podem ser gravados para filtrar os cabeçalhos de função em um arquivo de texto separado que pode servir como base para um documento de especificação.</span><span class="sxs-lookup"><span data-stu-id="b2149-190">For example, AWK scripts can be written to filter the function headers into a separate text file that can then serve as the basis for a specification document.</span></span> <span data-ttu-id="b2149-191">Da mesma forma, ferramentas como o utilitário autopato sem suporte (atualmente disponível no CD-ROM da biblioteca de desenvolvimento do Microsoft Developer Network) podem ser usadas para processar os blocos de comentário nesses cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="b2149-191">Similarly, tools like the unsupported AUTODUCK utility (currently available on the Microsoft Developer Network Development Library CD-ROM) can be used to process the comment blocks in these headers.</span></span>

<span data-ttu-id="b2149-192">A tabela a seguir lista as cadeias de caracteres de token iniciais e finais usadas em Tutoriais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="b2149-192">The following table lists beginning and ending token strings used in sample tutorials.</span></span>



| <span data-ttu-id="b2149-193">Token</span><span class="sxs-lookup"><span data-stu-id="b2149-193">Token</span></span> | <span data-ttu-id="b2149-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2149-194">Description</span></span>                      |
|-------|----------------------------------|
| /\*+  | <span data-ttu-id="b2149-195">Início do cabeçalho do arquivo</span><span class="sxs-lookup"><span data-stu-id="b2149-195">File Header Begin</span></span>                |
| +\*/  | <span data-ttu-id="b2149-196">Fim do cabeçalho do arquivo</span><span class="sxs-lookup"><span data-stu-id="b2149-196">File Header End</span></span>                  |
| /\*-  | <span data-ttu-id="b2149-197">Início do cabeçalho de bloco de comentário simples</span><span class="sxs-lookup"><span data-stu-id="b2149-197">Plain comment block Header Begin</span></span> |
| -\*/  | <span data-ttu-id="b2149-198">Fim do cabeçalho de bloco de comentário simples</span><span class="sxs-lookup"><span data-stu-id="b2149-198">Plain comment block Header End</span></span>   |
| <span data-ttu-id="b2149-199">/\*&</span><span class="sxs-lookup"><span data-stu-id="b2149-199">/\*C</span></span>  | <span data-ttu-id="b2149-200">Início do cabeçalho da classe</span><span class="sxs-lookup"><span data-stu-id="b2149-200">Class Header Begin</span></span>               |
| <span data-ttu-id="b2149-201">&\*/</span><span class="sxs-lookup"><span data-stu-id="b2149-201">C\*/</span></span>  | <span data-ttu-id="b2149-202">Fim do cabeçalho de classe</span><span class="sxs-lookup"><span data-stu-id="b2149-202">Class Header End</span></span>                 |
| <span data-ttu-id="b2149-203">/\*D</span><span class="sxs-lookup"><span data-stu-id="b2149-203">/\*M</span></span>  | <span data-ttu-id="b2149-204">Início do cabeçalho do método</span><span class="sxs-lookup"><span data-stu-id="b2149-204">Method Header Begin</span></span>              |
| <span data-ttu-id="b2149-205">D\*/</span><span class="sxs-lookup"><span data-stu-id="b2149-205">M\*/</span></span>  | <span data-ttu-id="b2149-206">Fim do cabeçalho do método</span><span class="sxs-lookup"><span data-stu-id="b2149-206">Method Header End</span></span>                |
| <span data-ttu-id="b2149-207">/\*Fixo</span><span class="sxs-lookup"><span data-stu-id="b2149-207">/\*F</span></span>  | <span data-ttu-id="b2149-208">Início do cabeçalho da função</span><span class="sxs-lookup"><span data-stu-id="b2149-208">Function Header Begin</span></span>            |
| <span data-ttu-id="b2149-209">Fixo\*/</span><span class="sxs-lookup"><span data-stu-id="b2149-209">F\*/</span></span>  | <span data-ttu-id="b2149-210">Fim do cabeçalho de função</span><span class="sxs-lookup"><span data-stu-id="b2149-210">Function Header End</span></span>              |
| <span data-ttu-id="b2149-211">/\*Encontrei</span><span class="sxs-lookup"><span data-stu-id="b2149-211">/\*I</span></span>  | <span data-ttu-id="b2149-212">Início do cabeçalho da interface</span><span class="sxs-lookup"><span data-stu-id="b2149-212">Interface Header Begin</span></span>           |
| <span data-ttu-id="b2149-213">Encontrei\*/</span><span class="sxs-lookup"><span data-stu-id="b2149-213">I\*/</span></span>  | <span data-ttu-id="b2149-214">Fim do cabeçalho da interface</span><span class="sxs-lookup"><span data-stu-id="b2149-214">Interface Header End</span></span>             |
| <span data-ttu-id="b2149-215">/\*Minúscula</span><span class="sxs-lookup"><span data-stu-id="b2149-215">/\*O</span></span>  | <span data-ttu-id="b2149-216">Início do cabeçalho da classe de objeto COM</span><span class="sxs-lookup"><span data-stu-id="b2149-216">COM Object Class Header Begin</span></span>    |
| <span data-ttu-id="b2149-217">Minúscula\*/</span><span class="sxs-lookup"><span data-stu-id="b2149-217">O\*/</span></span>  | <span data-ttu-id="b2149-218">Fim do cabeçalho da classe de objeto COM</span><span class="sxs-lookup"><span data-stu-id="b2149-218">COM Object Class Header End</span></span>      |



 

<span data-ttu-id="b2149-219">Esses cabeçalhos também podem ser usados como indicações visuais para verificação rápida de arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="b2149-219">These headers can also be used as visual cues for rapid scanning of source files.</span></span> <span data-ttu-id="b2149-220">Eles também fornecem conveniência para obter rapidamente um local de origem se você configurar cadeias de caracteres de pesquisa em seu editor e depois repetir a última pesquisa para localizar esses cabeçalhos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b2149-220">They also provide convenience for rapidly getting to some source location if you set up search strings in your editor and then 'repeat last search' to quickly locate these headers.</span></span>

<span data-ttu-id="b2149-221">Por exemplo, a cadeia de caracteres de pesquisa "M + M" localizará o início dos cabeçalhos de método e "M-M" localizará o início do código de definição/implementação do método real.</span><span class="sxs-lookup"><span data-stu-id="b2149-221">For example, the search string "M+M" will locate the start of method headers, and "M-M" will locate the beginning of the actual method definition/implementation code.</span></span>

 

 




