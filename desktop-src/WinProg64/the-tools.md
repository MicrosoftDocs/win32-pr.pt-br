---
title: As ferramentas
description: Este tópico descreve as ferramentas disponíveis para você usar o para tornar seu aplicativo 64-bit pronto. O Windows 10 está disponível para processadores baseados em x64 e ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guia de programação do Windows de 64 bits – programação do Windows de 64 bits, ferramentas
- ferramentas de programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364290"
---
# <a name="the-tools"></a><span data-ttu-id="8b39b-106">As ferramentas</span><span class="sxs-lookup"><span data-stu-id="8b39b-106">The Tools</span></span>

<span data-ttu-id="8b39b-107">Este tópico descreve as ferramentas disponíveis para você usar o para tornar seu aplicativo 64-bit pronto.</span><span class="sxs-lookup"><span data-stu-id="8b39b-107">This topic describes the tools available for you to use in making your application 64-bit ready.</span></span> <span data-ttu-id="8b39b-108">O Windows 10 está disponível para processadores baseados em x64 e ARM64.</span><span class="sxs-lookup"><span data-stu-id="8b39b-108">Windows 10 is available for both x64 and ARM64 based processors.</span></span>

## <a name="include-files"></a><span data-ttu-id="8b39b-109">Arquivos de inclusão</span><span class="sxs-lookup"><span data-stu-id="8b39b-109">Include Files</span></span>

<span data-ttu-id="8b39b-110">Os elementos da API são praticamente idênticos entre as janelas de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-110">The API elements are virtually identical between 32- and 64-bit Windows.</span></span> <span data-ttu-id="8b39b-111">Os arquivos de cabeçalho do Windows foram modificados para que possam ser usados para o código de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-111">The Windows header files have been modified so that they can be used for both 32- and 64-bit code.</span></span> <span data-ttu-id="8b39b-112">Os novos tipos de 64 bits e as macros são definidos em um novo arquivo de cabeçalho, Basetsd. h, que está no conjunto de arquivos de cabeçalho incluídos pelo Windows. h.</span><span class="sxs-lookup"><span data-stu-id="8b39b-112">The new 64-bit types and macros are defined in a new header file, Basetsd.h, which is in the set of header files included by Windows.h.</span></span> <span data-ttu-id="8b39b-113">O Basetsd. h inclui as novas definições de tipo de dados para ajudar a tornar independente o tamanho do Word do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="8b39b-113">Basetsd.h includes the new data-type definitions to assist in making source code word-size independent.</span></span>

## <a name="new-data-types"></a><span data-ttu-id="8b39b-114">Novos tipos de dados</span><span class="sxs-lookup"><span data-stu-id="8b39b-114">New Data Types</span></span>

<span data-ttu-id="8b39b-115">Os arquivos de cabeçalho do Windows contêm novos tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="8b39b-115">The Windows header files contain new data types.</span></span> <span data-ttu-id="8b39b-116">Esses tipos são principalmente para compatibilidade de tipo com os tipos de dados de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-116">These types are primarily for type compatibility with the 32-bit data types.</span></span> <span data-ttu-id="8b39b-117">Os novos tipos fornecem exatamente a mesma digitação dos tipos existentes, enquanto ao mesmo tempo fornecem suporte para o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-117">The new types provide exactly the same typing as the existing types, while at the same time providing support for the 64-bit Windows.</span></span> <span data-ttu-id="8b39b-118">Para obter mais informações, consulte [os novos tipos de dados](the-new-data-types.md) ou o arquivo de cabeçalho Basetsd. h.</span><span class="sxs-lookup"><span data-stu-id="8b39b-118">For more information, see [The New Data Types](the-new-data-types.md) or the Basetsd.h header file.</span></span>

## <a name="predefined-macros"></a><span data-ttu-id="8b39b-119">Macros predefinidas</span><span class="sxs-lookup"><span data-stu-id="8b39b-119">Predefined Macros</span></span>

<span data-ttu-id="8b39b-120">O compilador define as macros a seguir para identificar a plataforma.</span><span class="sxs-lookup"><span data-stu-id="8b39b-120">The compiler defines the following macros to identify the platform.</span></span>



| <span data-ttu-id="8b39b-121">Macro</span><span class="sxs-lookup"><span data-stu-id="8b39b-121">Macro</span></span>   | <span data-ttu-id="8b39b-122">Significado</span><span class="sxs-lookup"><span data-stu-id="8b39b-122">Meaning</span></span>                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b39b-123">\_WIN64</span><span class="sxs-lookup"><span data-stu-id="8b39b-123">\_WIN64</span></span> | <span data-ttu-id="8b39b-124">Uma plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-124">A 64-bit platform.</span></span> <span data-ttu-id="8b39b-125">Isso inclui x64 e ARM64.</span><span class="sxs-lookup"><span data-stu-id="8b39b-125">This includes both x64 and ARM64.</span></span>                                                        |
| <span data-ttu-id="8b39b-126">\_WIN32</span><span class="sxs-lookup"><span data-stu-id="8b39b-126">\_WIN32</span></span> | <span data-ttu-id="8b39b-127">Uma plataforma de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-127">A 32-bit platform.</span></span> <span data-ttu-id="8b39b-128">Esse valor também é definido pelo compilador de 64 bits para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="8b39b-128">This value is also defined by the 64-bit compiler for backward compatibility.</span></span><br/> |
| <span data-ttu-id="8b39b-129">\_WIN16</span><span class="sxs-lookup"><span data-stu-id="8b39b-129">\_WIN16</span></span> | <span data-ttu-id="8b39b-130">Uma plataforma de 16 bits</span><span class="sxs-lookup"><span data-stu-id="8b39b-130">A 16-bit platform</span></span>                                                                                           |



 

<span data-ttu-id="8b39b-131">As macros a seguir são específicas para a arquitetura.</span><span class="sxs-lookup"><span data-stu-id="8b39b-131">The following macros are specific to the architecture.</span></span>



| <span data-ttu-id="8b39b-132">Macro</span><span class="sxs-lookup"><span data-stu-id="8b39b-132">Macro</span></span>      | <span data-ttu-id="8b39b-133">Significado</span><span class="sxs-lookup"><span data-stu-id="8b39b-133">Meaning</span></span>                |
|------------|------------------------|
| <span data-ttu-id="8b39b-134">\_M \_ IA64</span><span class="sxs-lookup"><span data-stu-id="8b39b-134">\_M\_IA64</span></span>  | <span data-ttu-id="8b39b-135">Plataforma Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="8b39b-135">Intel Itanium platform</span></span> |
| <span data-ttu-id="8b39b-136">\_\_IX86 M</span><span class="sxs-lookup"><span data-stu-id="8b39b-136">\_M\_IX86</span></span>  | <span data-ttu-id="8b39b-137">plataforma x86</span><span class="sxs-lookup"><span data-stu-id="8b39b-137">x86 platform</span></span>           |
| <span data-ttu-id="8b39b-138">\_M \_ x64</span><span class="sxs-lookup"><span data-stu-id="8b39b-138">\_M\_X64</span></span>   | <span data-ttu-id="8b39b-139">plataforma x64</span><span class="sxs-lookup"><span data-stu-id="8b39b-139">x64 platform</span></span>           |
| <span data-ttu-id="8b39b-140">\_\_ARM64 M</span><span class="sxs-lookup"><span data-stu-id="8b39b-140">\_M\_ARM64</span></span> | <span data-ttu-id="8b39b-141">Plataforma ARM64</span><span class="sxs-lookup"><span data-stu-id="8b39b-141">ARM64 platform</span></span>         |



 

<span data-ttu-id="8b39b-142">Não use essas macros, exceto o código específico da arquitetura, em vez disso, use \_ Win64, \_ Win32 e \_ WIN16 sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="8b39b-142">Do not use these macros except with architecture-specific code, instead, use \_WIN64, \_WIN32, and \_WIN16 whenever possible.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="8b39b-143">Funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="8b39b-143">Helper Functions</span></span>

<span data-ttu-id="8b39b-144">As seguintes funções embutidas (definidas em Basetsd. h) podem ajudá-lo a converter com segurança valores de um tipo para outro.</span><span class="sxs-lookup"><span data-stu-id="8b39b-144">The following inline functions (defined in Basetsd.h) can help you safely convert values from one type to another.</span></span>

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> <span data-ttu-id="8b39b-145">**IntToPtr** Sign-estende o valor **int** , **UIntToPtr** zero-estende o valor **int não assinado** , **LongToPtr** de entrada-estende o valor **longo** e **ULongToPtr** zero estende o valor **longo não atribuído** .</span><span class="sxs-lookup"><span data-stu-id="8b39b-145">**IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.</span></span>

 

## <a name="64-bit-compiler"></a><span data-ttu-id="8b39b-146">Compilador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="8b39b-146">64-bit Compiler</span></span>

<span data-ttu-id="8b39b-147">Os compiladores de 64 bits podem ser usados para identificar o truncamento do ponteiro, as conversões incorretas de tipo e outros problemas específicos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-147">The 64-bit compilers can be used to identify pointer truncation, improper type casts, and other 64-bit-specific problems.</span></span>

<span data-ttu-id="8b39b-148">Quando o compilador é executado pela primeira vez, ele provavelmente gerará muitos avisos de truncamento de ponteiro ou de tipo incompatível, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8b39b-148">When the compiler is first run, it will probably generate many pointer truncation or type mismatch warnings, such as the following:</span></span>

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

<span data-ttu-id="8b39b-149">Use esses avisos como um guia para tornar o código mais robusto.</span><span class="sxs-lookup"><span data-stu-id="8b39b-149">Use these warnings as a guide to make the code more robust.</span></span> <span data-ttu-id="8b39b-150">É uma boa prática eliminar todos os avisos, especialmente avisos de truncamento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="8b39b-150">It is good practice to eliminate all warnings, especially pointer-truncation warnings.</span></span>

## <a name="64-bit-compiler-switches-and-warnings"></a><span data-ttu-id="8b39b-151">Opções e avisos do compilador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="8b39b-151">64-bit Compiler Switches and Warnings</span></span>

<span data-ttu-id="8b39b-152">Observe que esse compilador habilita o modelo de dados LLP64.</span><span class="sxs-lookup"><span data-stu-id="8b39b-152">Note that this compiler enables the LLP64 data model.</span></span>

<span data-ttu-id="8b39b-153">Há uma opção de aviso para ajudar a portar para o LLP64.</span><span class="sxs-lookup"><span data-stu-id="8b39b-153">There is a warning option to assist porting to LLP64.</span></span> <span data-ttu-id="8b39b-154">A opção-Wp64-w3 habilita os seguintes avisos:</span><span class="sxs-lookup"><span data-stu-id="8b39b-154">The -Wp64 -W3 switch enables the following warnings:</span></span>

-   <span data-ttu-id="8b39b-155">C4305: aviso de truncamento.</span><span class="sxs-lookup"><span data-stu-id="8b39b-155">C4305: Truncation warning.</span></span> <span data-ttu-id="8b39b-156">Por exemplo, "Return": truncamento de "Int64 não assinado" para "Long".</span><span class="sxs-lookup"><span data-stu-id="8b39b-156">For example, "return": truncation from "unsigned int64" to "long."</span></span>
-   <span data-ttu-id="8b39b-157">C4311: aviso de truncamento.</span><span class="sxs-lookup"><span data-stu-id="8b39b-157">C4311: Truncation warning.</span></span> <span data-ttu-id="8b39b-158">Por exemplo, "tipo Cast": truncamento de ponteiro de "int \* \_ ptr64" para "int".</span><span class="sxs-lookup"><span data-stu-id="8b39b-158">For example, "type cast": pointer truncation from "int\*\_ptr64" to "int."</span></span>
-   <span data-ttu-id="8b39b-159">C4312: conversão para aviso de tamanho maior.</span><span class="sxs-lookup"><span data-stu-id="8b39b-159">C4312: Conversion to bigger-size warning.</span></span> <span data-ttu-id="8b39b-160">Por exemplo, "tipo Cast": conversão de "int" para "int \* \_ ptr64" de tamanho maior.</span><span class="sxs-lookup"><span data-stu-id="8b39b-160">For example, "type cast": conversion from "int" to "int\*\_ptr64" of greater size.</span></span>
-   <span data-ttu-id="8b39b-161">C4318: passando comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="8b39b-161">C4318: Passing zero length.</span></span> <span data-ttu-id="8b39b-162">Por exemplo, passar constante zero como o comprimento para a função **memset** .</span><span class="sxs-lookup"><span data-stu-id="8b39b-162">For example, passing constant zero as the length to the **memset** function.</span></span>
-   <span data-ttu-id="8b39b-163">C4319: operador NOT.</span><span class="sxs-lookup"><span data-stu-id="8b39b-163">C4319: Not operator.</span></span> <span data-ttu-id="8b39b-164">Por exemplo, "~": zero estendendo "sem sinal" longo para "Int64 não assinado" \_ de tamanho maior.</span><span class="sxs-lookup"><span data-stu-id="8b39b-164">For example, "~": zero extending "unsigned long" to "unsigned \_int64" of greater size.</span></span>
-   <span data-ttu-id="8b39b-165">C4313: chamando a família de funções **printf** com especificadores e argumentos de tipo de conversão conflitantes.</span><span class="sxs-lookup"><span data-stu-id="8b39b-165">C4313: Calling the **printf** family of functions with conflicting conversion type specifiers and arguments.</span></span> <span data-ttu-id="8b39b-166">Por exemplo, "printf": "% p" na cadeia de caracteres de formato está em conflito com o argumento 2 do tipo " \_ Int64".</span><span class="sxs-lookup"><span data-stu-id="8b39b-166">For example, "printf": "%p" in format string conflicts with argument 2 of type "\_int64."</span></span> <span data-ttu-id="8b39b-167">Outro exemplo é a chamada printf ("% x", valor de ponteiro \_ ); isso causa um truncamento dos bits 32 superiores.</span><span class="sxs-lookup"><span data-stu-id="8b39b-167">Another example is the call printf("%x", pointer\_value); this causes a truncation of the upper 32 bits.</span></span> <span data-ttu-id="8b39b-168">A chamada correta é printf ("% p", valor de ponteiro \_ ).</span><span class="sxs-lookup"><span data-stu-id="8b39b-168">The correct call is printf("%p", pointer\_value).</span></span>
-   <span data-ttu-id="8b39b-169">C4244: igual ao C4242 de aviso existente.</span><span class="sxs-lookup"><span data-stu-id="8b39b-169">C4244: Same as the existing warning C4242.</span></span> <span data-ttu-id="8b39b-170">Por exemplo, "Return": conversão de " \_ Int64" para "int sem sinal", possível perda de dados.</span><span class="sxs-lookup"><span data-stu-id="8b39b-170">For example, "return": conversion from "\_int64" to "unsigned int," possible loss of data.</span></span>

## <a name="64-bit-linker-and-libraries"></a><span data-ttu-id="8b39b-171">Bibliotecas e vinculadores de 64 bits</span><span class="sxs-lookup"><span data-stu-id="8b39b-171">64-bit Linker and Libraries</span></span>

<span data-ttu-id="8b39b-172">Para compilar aplicativos, use o vinculador e as bibliotecas fornecidas pelo SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b39b-172">To build applications, use the linker and libraries provided by the Windows SDK.</span></span> <span data-ttu-id="8b39b-173">A maioria das bibliotecas de 32 bits tem uma versão de 64 bits correspondente, mas determinadas bibliotecas herdadas estão disponíveis somente em versões de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-173">Most 32-bit libraries have a corresponding 64-bit version, but certain legacy libraries are available only in 32-bit versions.</span></span> <span data-ttu-id="8b39b-174">O código que chama essas bibliotecas não será vinculado quando o aplicativo for compilado para o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8b39b-174">Code that calls into these libraries will not link when the application is built for 64-bit Windows.</span></span>

 

 





