---
title: Rotina de _allmul
description: Multiplica dois inteiros LONGLONG ou ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104007025"
---
# <a name="_allmul-routine"></a><span data-ttu-id="37ebc-103">\_Rotina allmul</span><span class="sxs-lookup"><span data-stu-id="37ebc-103">\_allmul Routine</span></span>

<span data-ttu-id="37ebc-104">Multiplica dois inteiros **LONGLONG** ou **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="37ebc-104">Multiplies two **LONGLONG** or **ULONGLONG** integers.</span></span>
<span data-ttu-id="37ebc-105">Por exemplo, para multiplicar dois valores Int64, o compilador pode gerar uma chamada para a rotina **\_ allmul** .</span><span class="sxs-lookup"><span data-stu-id="37ebc-105">For example, to multiply two int64 values the compiler might generate a call to the **\_allmul** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="37ebc-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="37ebc-106">Remarks</span></span>

<span data-ttu-id="37ebc-107">A rotina **\_ allmul** é uma rotina auxiliar para o compilador C.</span><span class="sxs-lookup"><span data-stu-id="37ebc-107">The **\_allmul** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="37ebc-108">Se o compilador usa **\_ allmul** é completamente dependente do conjunto de otimização.</span><span class="sxs-lookup"><span data-stu-id="37ebc-108">Whether the compiler uses **\_allmul** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="37ebc-109">Essa rotina é usada somente em plataformas x86.</span><span class="sxs-lookup"><span data-stu-id="37ebc-109">This routine is used only on x86 platforms.</span></span>
