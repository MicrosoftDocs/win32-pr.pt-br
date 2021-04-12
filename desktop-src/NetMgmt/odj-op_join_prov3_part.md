---
title: OP_JOINPROV3_PART
description: Definição de IDL de OP_JOINPROV3_PART
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104366866"
---
# <a name="op_joinprov3_part-structure"></a><span data-ttu-id="51ba8-103">Estrutura de OP_JOINPROV3_PART</span><span class="sxs-lookup"><span data-stu-id="51ba8-103">OP_JOINPROV3_PART structure</span></span>

<span data-ttu-id="51ba8-104">Contém informações adicionais usadas para configurar um cliente associado a um domínio.</span><span class="sxs-lookup"><span data-stu-id="51ba8-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ba8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51ba8-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a><span data-ttu-id="51ba8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="51ba8-106">Members</span></span>

### <a name="rid"></a><span data-ttu-id="51ba8-107">Eliminá</span><span class="sxs-lookup"><span data-stu-id="51ba8-107">Rid</span></span>

<span data-ttu-id="51ba8-108">Deve ser definido como o identificador relativo do SID da conta do computador</span><span class="sxs-lookup"><span data-stu-id="51ba8-108">Must be set to the Relative Identifier of the machine account’s SID</span></span>

### <a name="lpsid"></a><span data-ttu-id="51ba8-109">lpSid</span><span class="sxs-lookup"><span data-stu-id="51ba8-109">lpSid</span></span>

<span data-ttu-id="51ba8-110">Deve ser definido como o SID da conta do computador no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="51ba8-110">Must be set to the SID of the machine account in string form.</span></span>

## <a name="see-also"></a><span data-ttu-id="51ba8-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="51ba8-111">See also</span></span>

[<span data-ttu-id="51ba8-112">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="51ba8-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
