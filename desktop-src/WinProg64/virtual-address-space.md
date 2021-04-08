---
title: Espaço de endereço virtual (guia de programação para Windows de 64 bits)
description: Por padrão, aplicativos baseados no Microsoft Windows de 64 bits têm um espaço de endereço de modo de usuário de vários terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guia de programação do Windows de 64 bits, programação do Windows de 64 bits, espaço de endereço virtual
- espaço de endereço virtual programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008670"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a><span data-ttu-id="2704a-105">Espaço de endereço virtual (guia de programação para Windows de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="2704a-105">Virtual Address Space (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="2704a-106">Por padrão, aplicativos baseados no Microsoft Windows de 64 bits têm um espaço de endereço de modo de usuário de vários terabytes.</span><span class="sxs-lookup"><span data-stu-id="2704a-106">By default, 64-bit Microsoft Windows-based applications have a user-mode address space of several terabytes.</span></span> <span data-ttu-id="2704a-107">Para obter valores precisos, consulte [limites de memória para versões do Windows e do Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases).</span><span class="sxs-lookup"><span data-stu-id="2704a-107">For precise values, see [Memory Limits for Windows and Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span></span> <span data-ttu-id="2704a-108">No entanto, os aplicativos podem especificar que o sistema deve alocar toda a memória para o aplicativo abaixo de 2 gigabytes.</span><span class="sxs-lookup"><span data-stu-id="2704a-108">However, applications can specify that the system should allocate all memory for the application below 2 gigabytes.</span></span> <span data-ttu-id="2704a-109">Esse recurso é benéfico para aplicativos de 64 bits se as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="2704a-109">This feature is beneficial for 64-bit applications if the following conditions are true:</span></span>

-   <span data-ttu-id="2704a-110">Um espaço de endereço de 2 GB é suficiente.</span><span class="sxs-lookup"><span data-stu-id="2704a-110">A 2 GB address space is sufficient.</span></span>
-   <span data-ttu-id="2704a-111">O código tem muitos avisos de truncamento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="2704a-111">The code has many pointer truncation warnings.</span></span>
-   <span data-ttu-id="2704a-112">Ponteiros e inteiros são misturados livremente.</span><span class="sxs-lookup"><span data-stu-id="2704a-112">Pointers and integers are freely mixed.</span></span>
-   <span data-ttu-id="2704a-113">O código tem polimorfismo usando tipos de dados de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2704a-113">The code has polymorphism using 32-bit data types.</span></span>

<span data-ttu-id="2704a-114">Todos os ponteiros ainda são ponteiros de 64 bits, mas o sistema garante que cada alocação de memória ocorra abaixo do limite de 2 GB, de modo que, se o aplicativo truncar um ponteiro, nenhum dado significativo será perdido.</span><span class="sxs-lookup"><span data-stu-id="2704a-114">All pointers are still 64-bit pointers, but the system ensures that every memory allocation occurs below the 2 GB limit, so that if the application truncates a pointer, no significant data is lost.</span></span> <span data-ttu-id="2704a-115">Os ponteiros podem ser truncados para valores de 32 bits e estendidos para valores de 64 bits por extensão de assinatura ou extensão zero.</span><span class="sxs-lookup"><span data-stu-id="2704a-115">Pointers can be truncated to 32-bit values, then extended to 64-bit values by either sign extension or zero extension.</span></span>

<span data-ttu-id="2704a-116">Para especificar essa limitação de memória, use a opção **/LARGEADDRESSAWARE: no** linker.</span><span class="sxs-lookup"><span data-stu-id="2704a-116">To specify this memory limitation, use the **/LARGEADDRESSAWARE:NO** linker option.</span></span> <span data-ttu-id="2704a-117">Observe que **/LARGEADDRESSAWARE: no** é ignorado para um binário ARM64.</span><span class="sxs-lookup"><span data-stu-id="2704a-117">Note that **/LARGEADDRESSAWARE:NO** is ignored for an ARM64 binary.</span></span> <span data-ttu-id="2704a-118">No entanto, lembre-se de que podem ocorrer problemas ao usar essa opção.</span><span class="sxs-lookup"><span data-stu-id="2704a-118">However, be aware that problems can occur when using this option.</span></span> <span data-ttu-id="2704a-119">Se você criar uma DLL que usa essa opção e a DLL for chamada por um aplicativo que não usa essa opção, a DLL poderá truncar um ponteiro de 64 bits cujos bits superiores 32 sejam significativos.</span><span class="sxs-lookup"><span data-stu-id="2704a-119">If you build a DLL that uses this option and the DLL is called by an application that does not use this option, the DLL could truncate a 64-bit pointer whose upper 32 bits are significant.</span></span> <span data-ttu-id="2704a-120">Isso pode causar falha no aplicativo sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="2704a-120">This can cause application failure without any warning.</span></span>

 

 
