---
title: Diretivas de pré-processador (HLSL)
description: Diretivas de pré-processador, como \ define e \ ifdef, normalmente são usadas para tornar os programas de origem fáceis de alterar e fáceis de compilar em ambientes de execução diferentes.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386825"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="8db3f-103">Diretivas de pré-processador (HLSL)</span><span class="sxs-lookup"><span data-stu-id="8db3f-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="8db3f-104">Diretivas de pré-processador, como [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), normalmente são usadas para facilitar a alteração dos programas de origem e fácil de compilar em ambientes de execução diferentes.</span><span class="sxs-lookup"><span data-stu-id="8db3f-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="8db3f-105">As políticas no arquivo de origem mandam o pré-processador realizar ações específicas.</span><span class="sxs-lookup"><span data-stu-id="8db3f-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="8db3f-106">Por exemplo, o pré-processador pode substituir tokens no texto, inserir o conteúdo de outros arquivos no arquivo de origem ou suprimir a compilação de parte do arquivo removendo seções de texto.</span><span class="sxs-lookup"><span data-stu-id="8db3f-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="8db3f-107">As linhas do pré-processador são reconhecidas e executadas antes de expansão macro.</span><span class="sxs-lookup"><span data-stu-id="8db3f-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="8db3f-108">Portanto, se uma macro se expandir até algo que se pareça com um comando do pré-processador, esse comando não será reconhecido pelo pré-processador.</span><span class="sxs-lookup"><span data-stu-id="8db3f-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="8db3f-109">As instruções do pré-processador usam o mesmo conjunto de caracteres das instruções de arquivo de origem, com exceção das sequências de escape, que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="8db3f-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="8db3f-110">O conjunto de caracteres usado em instruções do pré-processador é igual ao conjunto de caracteres de execução.</span><span class="sxs-lookup"><span data-stu-id="8db3f-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="8db3f-111">O pré-processador também reconhece valores negativos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8db3f-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="8db3f-112">O pré-processador HLSL reconhece as seguintes diretivas:</span><span class="sxs-lookup"><span data-stu-id="8db3f-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="8db3f-113">\#Definir</span><span class="sxs-lookup"><span data-stu-id="8db3f-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="8db3f-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="8db3f-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="8db3f-115">\#else</span><span class="sxs-lookup"><span data-stu-id="8db3f-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="8db3f-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="8db3f-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="8db3f-117">\#Erro</span><span class="sxs-lookup"><span data-stu-id="8db3f-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="8db3f-118">\#Se</span><span class="sxs-lookup"><span data-stu-id="8db3f-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="8db3f-119">\#Ifdef</span><span class="sxs-lookup"><span data-stu-id="8db3f-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="8db3f-120">\#Ifndef</span><span class="sxs-lookup"><span data-stu-id="8db3f-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="8db3f-121">\#Incluem</span><span class="sxs-lookup"><span data-stu-id="8db3f-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="8db3f-122">\#line</span><span class="sxs-lookup"><span data-stu-id="8db3f-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="8db3f-123">\#Pragma</span><span class="sxs-lookup"><span data-stu-id="8db3f-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="8db3f-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="8db3f-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="8db3f-125">O sinal de número ( ) deve ser o primeiro caractere de espaço não branco na linha que contém a diretiva ; os caracteres de espaço em branco podem aparecer entre o sinal de número e a primeira letra da \# diretiva.</span><span class="sxs-lookup"><span data-stu-id="8db3f-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="8db3f-126">Algumas políticas incluem argumentos ou valores.</span><span class="sxs-lookup"><span data-stu-id="8db3f-126">Some directives include arguments or values.</span></span> <span data-ttu-id="8db3f-127">Qualquer texto que siga uma diretiva (exceto um argumento ou valor que faz parte da diretiva) deve ser precedido pelo delimitador de comentário de linha única (//) ou incluído nos delimitadores de comentário (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="8db3f-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="8db3f-128">As linhas que contêm diretivas de pré-processador podem ser continuadas precedendo imediatamente o marcador de fim de linha com uma faixa invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="8db3f-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\\).</span></span>

<span data-ttu-id="8db3f-129">As políticas do pré-processador podem aparecer em qualquer lugar do arquivo de origem, mas se aplicam somente ao restante dele.</span><span class="sxs-lookup"><span data-stu-id="8db3f-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8db3f-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8db3f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db3f-131">Apêndice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8db3f-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




