---
title: Diretivas de pré-processador (HLSL)
description: As diretivas de pré-processador, como \ definir e \ ifdef, normalmente são usadas para facilitar a alteração e a facilidade dos programas de origem em ambientes de execução diferentes.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644082"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="23dd9-103">Diretivas de pré-processador (HLSL)</span><span class="sxs-lookup"><span data-stu-id="23dd9-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="23dd9-104">As diretivas de pré-processador, como [ \# definir](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), normalmente são usadas para tornar os programas de origem fáceis de alterar e fáceis de Compilar em ambientes de execução diferentes.</span><span class="sxs-lookup"><span data-stu-id="23dd9-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="23dd9-105">As políticas no arquivo de origem mandam o pré-processador realizar ações específicas.</span><span class="sxs-lookup"><span data-stu-id="23dd9-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="23dd9-106">Por exemplo, o pré-processador pode substituir tokens no texto, inserir o conteúdo de outros arquivos no arquivo de origem ou suprimir a compilação de parte do arquivo removendo seções de texto.</span><span class="sxs-lookup"><span data-stu-id="23dd9-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="23dd9-107">As linhas do pré-processador são reconhecidas e executadas antes de expansão macro.</span><span class="sxs-lookup"><span data-stu-id="23dd9-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="23dd9-108">Portanto, se uma macro se expandir até algo que se pareça com um comando do pré-processador, esse comando não será reconhecido pelo pré-processador.</span><span class="sxs-lookup"><span data-stu-id="23dd9-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="23dd9-109">As instruções do pré-processador usam o mesmo conjunto de caracteres das instruções de arquivo de origem, com exceção das sequências de escape, que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="23dd9-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="23dd9-110">O conjunto de caracteres usado em instruções do pré-processador é igual ao conjunto de caracteres de execução.</span><span class="sxs-lookup"><span data-stu-id="23dd9-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="23dd9-111">O pré-processador também reconhece valores negativos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="23dd9-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="23dd9-112">O pré-processador HLSL reconhece as seguintes diretivas:</span><span class="sxs-lookup"><span data-stu-id="23dd9-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="23dd9-113">\#definir</span><span class="sxs-lookup"><span data-stu-id="23dd9-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="23dd9-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="23dd9-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="23dd9-115">\#else</span><span class="sxs-lookup"><span data-stu-id="23dd9-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="23dd9-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="23dd9-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="23dd9-117">\#ao</span><span class="sxs-lookup"><span data-stu-id="23dd9-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="23dd9-118">\#que</span><span class="sxs-lookup"><span data-stu-id="23dd9-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="23dd9-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="23dd9-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="23dd9-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="23dd9-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="23dd9-121">\#incluir</span><span class="sxs-lookup"><span data-stu-id="23dd9-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="23dd9-122">\#descritos</span><span class="sxs-lookup"><span data-stu-id="23dd9-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="23dd9-123">\#pragma</span><span class="sxs-lookup"><span data-stu-id="23dd9-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="23dd9-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="23dd9-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="23dd9-125">O sinal numérico ( \# ) deve ser o primeiro caractere que não seja de espaço em branco na linha que contém a diretiva; caracteres de espaço em branco podem aparecer entre o sinal numérico e a primeira letra da diretiva.</span><span class="sxs-lookup"><span data-stu-id="23dd9-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="23dd9-126">Algumas políticas incluem argumentos ou valores.</span><span class="sxs-lookup"><span data-stu-id="23dd9-126">Some directives include arguments or values.</span></span> <span data-ttu-id="23dd9-127">Qualquer texto que segue uma diretiva (exceto um argumento ou valor que faça parte da diretiva) deve ser precedido pelo delimitador de comentário de linha única (//) ou colocado em delimitadores de comentário (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="23dd9-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="23dd9-128">As linhas que contêm diretivas de pré-processador podem ser continuadas imediatamente antes do marcador de fim de linha com uma barra invertida ( \) .</span><span class="sxs-lookup"><span data-stu-id="23dd9-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\).</span></span>

<span data-ttu-id="23dd9-129">As políticas do pré-processador podem aparecer em qualquer lugar do arquivo de origem, mas se aplicam somente ao restante dele.</span><span class="sxs-lookup"><span data-stu-id="23dd9-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23dd9-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23dd9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23dd9-131">Apêndice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23dd9-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




