---
title: Preparando seu aplicativo para o Windows de 64 bits
description: Há vários recursos que facilitam o desenvolvimento de aplicativos que serão executados em janelas de 32 e 64 bits. A maioria deles, como os novos tipos de dados, é descrita em preparando-se para o Windows de 64 bits.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Kit de ferramentas de 64 bits 64-programação do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162387"
---
# <a name="preparing-your-application-for-64-bit-windows"></a><span data-ttu-id="01787-105">Preparando seu aplicativo para o Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="01787-105">Preparing Your Application for 64-bit Windows</span></span>

<span data-ttu-id="01787-106">Há vários recursos que facilitam o desenvolvimento de aplicativos que serão executados em janelas de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="01787-106">There are several features that make it easier for you to develop applications that will run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="01787-107">A maioria deles, como os novos tipos de dados, é descrita em [preparando-se para o Windows de 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="01787-107">Most of these, such as the new data types, are described in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

<span data-ttu-id="01787-108">O kit de ferramentas de 64 bits fornecido com o SDK do Windows inclui um compilador de MIDL de 64 bits, Midl.exe, para gerar stubs de 64 bits nativos, bem como stubs de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="01787-108">The 64-bit toolkit that ships with the Windows SDK includes a 64-bit MIDL compiler, Midl.exe, for generating native 64-bit stubs, as well as 32-bit stubs.</span></span> <span data-ttu-id="01787-109">Use a opção **/env Win64** para gerar somente stubs de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="01787-109">Use the **/env win64** switch to generate 64-bit stubs only.</span></span> <span data-ttu-id="01787-110">O padrão é gerar stubs duplos que são executados em ambas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="01787-110">The default is to generate dual stubs that run on both platforms.</span></span>

<span data-ttu-id="01787-111">Observe que o MIDL de 64 bits dá suporte apenas aos modos de otimização [**/Oicf**](/windows/desktop/Midl/-oi) e [**/os**](/windows/desktop/Midl/-os) .</span><span class="sxs-lookup"><span data-stu-id="01787-111">Note that the 64-bit MIDL supports the [**/Oicf**](/windows/desktop/Midl/-oi) and [**/Os**](/windows/desktop/Midl/-os) optimization modes only.</span></span>

 

 