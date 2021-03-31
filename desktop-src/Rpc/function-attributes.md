---
title: Atributos de função
description: Os atributos \ callback \ e \ local \ podem ser aplicados como atributos de função.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641685"
---
# <a name="function-attributes"></a><span data-ttu-id="718b5-103">Atributos de função</span><span class="sxs-lookup"><span data-stu-id="718b5-103">Function Attributes</span></span>

<span data-ttu-id="718b5-104">O **\[** [**retorno de chamada**](/windows/desktop/Midl/callback) **\]** e os **\[** atributos [**locais**](/windows/desktop/Midl/local) **\]** podem ser aplicados como atributos de função.</span><span class="sxs-lookup"><span data-stu-id="718b5-104">The **\[**[**callback**](/windows/desktop/Midl/callback)**\]** and **\[**[**local**](/windows/desktop/Midl/local)**\]** attributes can be applied as function attributes.</span></span>

<span data-ttu-id="718b5-105">Um callback é uma chamada remota do servidor para o cliente que é executado como parte de um thread de execução única conceitual.</span><span class="sxs-lookup"><span data-stu-id="718b5-105">A callback is a remote call from server to client that executes as part of a conceptual single-execution thread.</span></span> <span data-ttu-id="718b5-106">Um retorno de chamada é sempre emitido no contexto de uma chamada remota (ou callback) e é executado pelo thread que emitiu a chamada remota original (ou retorno de chamada).</span><span class="sxs-lookup"><span data-stu-id="718b5-106">A callback is always issued in the context of a remote call (or callback) and is executed by the thread that issued the original remote call (or callback).</span></span>

<span data-ttu-id="718b5-107">Geralmente, é desejável posicionar uma declaração de procedimento local no arquivo IDL, já que esse é o local lógico para descrever as interfaces para um pacote.</span><span class="sxs-lookup"><span data-stu-id="718b5-107">It is often desirable to place a local procedure declaration in the IDL file, since this is the logical place to describe interfaces to a package.</span></span> <span data-ttu-id="718b5-108">O **\[** [](/windows/desktop/Midl/local) **\]** atributo local indica que uma declaração de procedimento não é, na verdade, uma função remota, mas um procedimento local.</span><span class="sxs-lookup"><span data-stu-id="718b5-108">The **\[**[**local**](/windows/desktop/Midl/local)**\]** attribute indicates that a procedure declaration is not actually a remote function, but a local procedure.</span></span> <span data-ttu-id="718b5-109">O compilador MIDL não gera stubs para funções com o atributo **\[ local \]** .</span><span class="sxs-lookup"><span data-stu-id="718b5-109">The MIDL compiler does not generate any stubs for functions with the **\[local\]** attribute.</span></span>

<span data-ttu-id="718b5-110">É importante observar que o uso de retorno de **\[** [**chamada**](/windows/desktop/Midl/callback) **\]** não é recomendado na programação de vários threads.</span><span class="sxs-lookup"><span data-stu-id="718b5-110">It is important to note that the use of **\[**[**callback**](/windows/desktop/Midl/callback)**\]** is not recommended in multi-thread programming.</span></span> <span data-ttu-id="718b5-111">Como uma função de programação de thread único, ele não está equipado para dar suporte às demandas de segurança que um ambiente de vários threads fornece.</span><span class="sxs-lookup"><span data-stu-id="718b5-111">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

 

 