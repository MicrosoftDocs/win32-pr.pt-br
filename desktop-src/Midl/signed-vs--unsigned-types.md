---
title: Tipos assinados e não assinados (MIDL)
description: Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipos de dados MIDL, assinados e não assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369062"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="c8dd0-104">Tipos assinados e não assinados (MIDL)</span><span class="sxs-lookup"><span data-stu-id="c8dd0-104">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="c8dd0-105">Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="c8dd0-106">Você pode evitar esses problemas declarando explicitamente seus tipos de caracteres como assinados ou não assinados.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-106">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="c8dd0-107">Observe que os compiladores de IDL do DCE não reconhecem a palavra-chave [**assinada**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="c8dd0-107">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="c8dd0-108">Portanto, esse recurso não está disponível quando você usa o compilador MIDL/opção **uso**</span><span class="sxs-lookup"><span data-stu-id="c8dd0-108">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="c8dd0-109">MIDL define o tipo [**pequeno**](small.md) para assumir o mesmo sinal padrão que o tipo [**Char**](char-idl.md) no compilador C de destino.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-109">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="c8dd0-110">Se o compilador assumir que **Char** não está assinado, **pequeno** também será definido como não assinado.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-110">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="c8dd0-111">Muitos compiladores do C permitem alterar o padrão como uma opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-111">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="c8dd0-112">Por exemplo, no ambiente de desenvolvimento Microsoft Visual C++, a opção de linha de comando **/j** altera o sinal padrão de **Char** de assinado para não assinado.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-112">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="c8dd0-113">Você também pode controlar o sinal de variáveis do tipo [**Char**](char-idl.md) e [**Small**](small.md) com a opção de linha de comando [**/Char**](-char.md)do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-113">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="c8dd0-114">Essa opção permite que você especifique o sinal padrão usado pelo seu compilador.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-114">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="c8dd0-115">O compilador MIDL declara explicitamente o sinal de todos os tipos **Char** que não correspondem ao tipo padrão do compilador C no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="c8dd0-115">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




