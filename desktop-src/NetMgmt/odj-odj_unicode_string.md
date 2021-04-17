---
title: ODJ_UNICODE_STRING
description: Definição de IDL de ODJ_UNICODE_STRING
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "105798320"
---
# <a name="odj_unicode_string-structure"></a><span data-ttu-id="40ecf-103">Estrutura de ODJ_UNICODE_STRING</span><span class="sxs-lookup"><span data-stu-id="40ecf-103">ODJ_UNICODE_STRING structure</span></span>

<span data-ttu-id="40ecf-104">Contém uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="40ecf-104">Contains a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ecf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40ecf-105">Syntax</span></span>

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a><span data-ttu-id="40ecf-106">Membros</span><span class="sxs-lookup"><span data-stu-id="40ecf-106">Members</span></span>

### <a name="length"></a><span data-ttu-id="40ecf-107">Comprimento</span><span class="sxs-lookup"><span data-stu-id="40ecf-107">Length</span></span>

<span data-ttu-id="40ecf-108">Deve ser definido como o número de bytes no buffer que contém a cadeia de caracteres, não incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="40ecf-108">Must be set to the number of bytes in Buffer containing the string, not including the NULL terminator.</span></span>

### <a name="maximumlength"></a><span data-ttu-id="40ecf-109">MaximumLength</span><span class="sxs-lookup"><span data-stu-id="40ecf-109">MaximumLength</span></span>

<span data-ttu-id="40ecf-110">Isso deve ser definido como o número total de bytes no buffer, não incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="40ecf-110">This MUST be set to the total number of bytes in Buffer, not including the NULL terminator.</span></span>

### <a name="buffer"></a><span data-ttu-id="40ecf-111">Buffer</span><span class="sxs-lookup"><span data-stu-id="40ecf-111">Buffer</span></span>

<span data-ttu-id="40ecf-112">Deve ser uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="40ecf-112">Must be a Unicode string.</span></span>

## <a name="see-also"></a><span data-ttu-id="40ecf-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="40ecf-113">See also</span></span>

[<span data-ttu-id="40ecf-114">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="40ecf-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
