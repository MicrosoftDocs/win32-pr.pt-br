---
title: OP_JOINPROV2_PART
description: Definição de IDL de OP_JOINPROV2_PART
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104084985"
---
# <a name="op_joinprov2_part-structure"></a><span data-ttu-id="ed570-103">Estrutura de OP_JOINPROV2_PART</span><span class="sxs-lookup"><span data-stu-id="ed570-103">OP_JOINPROV2_PART structure</span></span>

<span data-ttu-id="ed570-104">Contém informações adicionais usadas para configurar um cliente associado a um domínio.</span><span class="sxs-lookup"><span data-stu-id="ed570-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed570-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed570-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a><span data-ttu-id="ed570-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ed570-106">Members</span></span>

### <a name="dwflags"></a><span data-ttu-id="ed570-107">dwFlags</span><span class="sxs-lookup"><span data-stu-id="ed570-107">dwFlags</span></span>

<span data-ttu-id="ed570-108">Deve ser definido como zero ou um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ed570-108">Must be set to either zero or one of the following values:</span></span>

|<span data-ttu-id="ed570-109">Valor</span><span class="sxs-lookup"><span data-stu-id="ed570-109">Value</span></span>|<span data-ttu-id="ed570-110">Significado</span><span class="sxs-lookup"><span data-stu-id="ed570-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="ed570-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ed570-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span></span>|<span data-ttu-id="ed570-112">O site especificado em lpSiteName deve ser considerado o site permanente para o cliente.</span><span class="sxs-lookup"><span data-stu-id="ed570-112">The site specified in lpSiteName MUST be considered the permanent site for the client.</span></span>|

### <a name="lpnetbiosname"></a><span data-ttu-id="ed570-113">lpNetbiosName</span><span class="sxs-lookup"><span data-stu-id="ed570-113">lpNetbiosName</span></span>

<span data-ttu-id="ed570-114">Contém o nome NetBIOS da conta do computador no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ed570-114">Contains the Netbios name of the machine account in Unicode format.</span></span>

### <a name="lpsitename"></a><span data-ttu-id="ed570-115">lpSiteName</span><span class="sxs-lookup"><span data-stu-id="ed570-115">lpSiteName</span></span>

<span data-ttu-id="ed570-116">Contém o nome do site de Active Directory que o cliente deve usar.</span><span class="sxs-lookup"><span data-stu-id="ed570-116">Contains the name of the Active Directory site that the client should use.</span></span>

### <a name="lpprimarydnsdomain"></a><span data-ttu-id="ed570-117">lpPrimaryDNSDomain</span><span class="sxs-lookup"><span data-stu-id="ed570-117">lpPrimaryDNSDomain</span></span>

<span data-ttu-id="ed570-118">Contém o nome de domínio DNS primário que o cliente deve usar.</span><span class="sxs-lookup"><span data-stu-id="ed570-118">Contains the primary DNS domain name that the client should use.</span></span>

### <a name="dwreserved"></a><span data-ttu-id="ed570-119">dwReserved</span><span class="sxs-lookup"><span data-stu-id="ed570-119">dwReserved</span></span>

<span data-ttu-id="ed570-120">Reservado para uso futuro e deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="ed570-120">Reserved for future use and must be set to 0.</span></span>

### <a name="lpreserved"></a><span data-ttu-id="ed570-121">lpReserved</span><span class="sxs-lookup"><span data-stu-id="ed570-121">lpReserved</span></span>

<span data-ttu-id="ed570-122">Reservado para uso futuro e deve ser definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="ed570-122">Reserved for future use and must be set to NULL.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed570-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed570-123">See also</span></span>

[<span data-ttu-id="ed570-124">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="ed570-124">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
