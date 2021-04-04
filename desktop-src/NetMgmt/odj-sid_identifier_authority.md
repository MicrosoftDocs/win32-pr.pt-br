---
title: SID_IDENTIFIER_AUTHORITY
description: Definição de IDL de SID_IDENTIFIER_AUTHORITY
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104084986"
---
# <a name="sid_identifier_authority-structure"></a><span data-ttu-id="00180-103">Estrutura de SID_IDENTIFIER_AUTHORITY</span><span class="sxs-lookup"><span data-stu-id="00180-103">SID_IDENTIFIER_AUTHORITY structure</span></span>

<span data-ttu-id="00180-104">Contém uma autoridade de identificador SID.</span><span class="sxs-lookup"><span data-stu-id="00180-104">Contains a SID identifier authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="00180-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00180-105">Syntax</span></span>

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a><span data-ttu-id="00180-106">Membros</span><span class="sxs-lookup"><span data-stu-id="00180-106">Members</span></span>

### <a name="value"></a><span data-ttu-id="00180-107">Valor</span><span class="sxs-lookup"><span data-stu-id="00180-107">Value</span></span>

<span data-ttu-id="00180-108">Deve ser definido como os seis bytes da autoridade do identificador SID.</span><span class="sxs-lookup"><span data-stu-id="00180-108">Must be set to the six bytes of the SID identifier authority.</span></span>

## <a name="see-also"></a><span data-ttu-id="00180-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="00180-109">See also</span></span>

[<span data-ttu-id="00180-110">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="00180-110">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)