---
title: Tipos assinados e não assinados (RPC)
description: Saiba mais sobre tipos assinados e não assinados no RPC. Compiladores que usam tipos de padrões diferentes podem causar erros de software em seu aplicativo distribuído.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406539"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="4ddeb-104">Tipos assinados e não assinados (RPC)</span><span class="sxs-lookup"><span data-stu-id="4ddeb-104">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="4ddeb-105">Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="4ddeb-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="4ddeb-106">Você pode evitar esses problemas declarando explicitamente seus tipos de caracteres **como assinados** **ou sem sinal.**</span><span class="sxs-lookup"><span data-stu-id="4ddeb-106">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="4ddeb-107">MIDL define o [**tipo pequeno**](/windows/desktop/Midl/small) para assumir o mesmo sinal padrão que o tipo **char** no compilador C de destino.</span><span class="sxs-lookup"><span data-stu-id="4ddeb-107">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="4ddeb-108">Se o compilador assumir que **char** não foi assinado, **small** também será definido como sem-assinatura.</span><span class="sxs-lookup"><span data-stu-id="4ddeb-108">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="4ddeb-109">Muitos compiladores C permitem alterar o padrão como uma opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4ddeb-109">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="4ddeb-110">Por exemplo, a opção de linha de comando **/J** do compilador do Microsoft C altera o sinal padrão de **char** de assinado para não assinado.</span><span class="sxs-lookup"><span data-stu-id="4ddeb-110">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="4ddeb-111">Você também pode controlar o sinal de variáveis do tipo **char** e **small** com a opção de linha de comando do compilador MIDL [**/char**](/windows/desktop/Midl/-char).</span><span class="sxs-lookup"><span data-stu-id="4ddeb-111">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="4ddeb-112">Essa opção permite que você especifique o sinal padrão usado pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="4ddeb-112">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="4ddeb-113">O compilador MIDL declara explicitamente o sinal de todos os tipos **de caracteres** que não corresponderem ao tipo padrão do compilador C no arquivo de header gerado.</span><span class="sxs-lookup"><span data-stu-id="4ddeb-113">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
