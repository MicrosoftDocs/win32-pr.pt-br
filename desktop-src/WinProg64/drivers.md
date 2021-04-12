---
title: Drivers (guia de programação para o Windows de 64 bits)
description: A versão de 64 bits do Windows foi projetada para possibilitar que os desenvolvedores usem uma base de código-fonte única para seus aplicativos de 32 bits e de 64 bits. Para uma grande extensão, isso também é verdadeiro para drivers do Windows de 32 bits e 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- drivers de programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294726"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a><span data-ttu-id="fb759-105">Drivers (guia de programação para o Windows de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="fb759-105">Drivers (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="fb759-106">A versão de 64 bits do Windows foi projetada para possibilitar que os desenvolvedores usem uma base de código-fonte única para seus aplicativos de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb759-106">The 64-bit version of Windows is designed to make it possible for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="fb759-107">Para uma grande extensão, isso também é verdadeiro para drivers do Windows de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb759-107">To a large extent, this is also true for 32-bit and 64-bit Windows drivers.</span></span>

<span data-ttu-id="fb759-108">No entanto, os drivers de 32 bits não podem ser executados em janelas de 64 bits e devem ser portados.</span><span class="sxs-lookup"><span data-stu-id="fb759-108">However, 32-bit drivers cannot run on 64-bit Windows and must be ported.</span></span> <span data-ttu-id="fb759-109">Para aplicativos de modo de usuário, o Windows de 64 bits inclui o WOW64, que permite que aplicativos do Windows de 32 bits sejam executados (com alguma perda de desempenho) em sistemas que executam o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb759-109">For user-mode applications, 64-bit Windows includes WOW64, which enables 32-bit Windows applications to execute (with some loss of performance) on systems running 64-bit Windows.</span></span> <span data-ttu-id="fb759-110">Não existe nenhuma camada de conversão equivalente para os drivers.</span><span class="sxs-lookup"><span data-stu-id="fb759-110">No equivalent translation layer exists for drivers.</span></span>

<span data-ttu-id="fb759-111">Para obter informações sobre como portar drivers para o Windows de 64 bits, consulte [problemas de 64 bits](https://msdn.microsoft.com/library/aa489627.aspx) no WDK (Kit de driver do Windows).</span><span class="sxs-lookup"><span data-stu-id="fb759-111">For information about porting drivers to 64-bit Windows, see [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) in the Windows Driver Kit (WDK).</span></span>

 

 




