---
title: Tipos assinados e não assinados (RPC)
description: Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824120"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="b5893-103">Tipos assinados e não assinados (RPC)</span><span class="sxs-lookup"><span data-stu-id="b5893-103">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="b5893-104">Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="b5893-104">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="b5893-105">Você pode evitar esses problemas declarando explicitamente seus tipos de caracteres como **assinados** ou **não assinados**.</span><span class="sxs-lookup"><span data-stu-id="b5893-105">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="b5893-106">MIDL define o tipo [**pequeno**](/windows/desktop/Midl/small) para assumir o mesmo sinal padrão que o tipo **Char** no compilador C de destino.</span><span class="sxs-lookup"><span data-stu-id="b5893-106">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="b5893-107">Se o compilador assumir que **Char** não está assinado, **pequeno** também será definido como não assinado.</span><span class="sxs-lookup"><span data-stu-id="b5893-107">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="b5893-108">Muitos compiladores do C permitem alterar o padrão como uma opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b5893-108">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="b5893-109">Por exemplo, a opção de linha de comando Microsoft C Compiler **/j** altera o sinal padrão de **Char** de assinado para não assinado.</span><span class="sxs-lookup"><span data-stu-id="b5893-109">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="b5893-110">Você também pode controlar o sinal de variáveis do tipo **Char** e **Small** com a opção de linha de comando [**/Char**](/windows/desktop/Midl/-char)do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="b5893-110">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="b5893-111">Essa opção permite que você especifique o sinal padrão usado pelo seu compilador.</span><span class="sxs-lookup"><span data-stu-id="b5893-111">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="b5893-112">O compilador MIDL declara explicitamente o sinal de todos os tipos **Char** que não correspondem ao tipo padrão do compilador C no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="b5893-112">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
