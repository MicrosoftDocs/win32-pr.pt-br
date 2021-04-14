---
title: Rotina de _aulldiv
description: Divide dois inteiros ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104453836"
---
# <a name="_aulldiv-routine"></a><span data-ttu-id="8e72b-103">\_Rotina aulldiv</span><span class="sxs-lookup"><span data-stu-id="8e72b-103">\_aulldiv Routine</span></span>

<span data-ttu-id="8e72b-104">Divide dois inteiros **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="8e72b-104">Divides two **ULONGLONG** integers.</span></span>
<span data-ttu-id="8e72b-105">Por exemplo, para dividir dois valores UInt64, o compilador pode gerar uma chamada para a rotina **\_ aulldiv** .</span><span class="sxs-lookup"><span data-stu-id="8e72b-105">For example, to divide two uint64 values the compiler might generate a call to the **\_aulldiv** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e72b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e72b-106">Remarks</span></span>

<span data-ttu-id="8e72b-107">A rotina **\_ aulldiv** é uma rotina auxiliar para o compilador C.</span><span class="sxs-lookup"><span data-stu-id="8e72b-107">The **\_aulldiv** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="8e72b-108">Se o compilador usa **\_ aulldiv** é completamente dependente do conjunto de otimização.</span><span class="sxs-lookup"><span data-stu-id="8e72b-108">Whether the compiler uses **\_aulldiv** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="8e72b-109">Essa função é usada somente em plataformas x86.</span><span class="sxs-lookup"><span data-stu-id="8e72b-109">This function is used only on x86 platforms.</span></span>
