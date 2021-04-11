---
title: Estrutura de MPTHREAT_INFOEX_NIS (MpClient. h)
description: Contém informações específicas do NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_INFOEX_NIS
- Ponteiro de estrutura de PMPTHREAT_INFOEX_NIS recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009316"
---
# <a name="mpthreat_infoex_nis-structure"></a><span data-ttu-id="c39c4-105">\_Estrutura MPTHREAT INFOEX \_ NIS</span><span class="sxs-lookup"><span data-stu-id="c39c4-105">MPTHREAT\_INFOEX\_NIS structure</span></span>

<span data-ttu-id="c39c4-106">Contém informações específicas do NIS.</span><span class="sxs-lookup"><span data-stu-id="c39c4-106">Contains NIS-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c39c4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c39c4-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a><span data-ttu-id="c39c4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c39c4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c39c4-109">**SourceIP**</span><span class="sxs-lookup"><span data-stu-id="c39c4-109">**SourceIP**</span></span>
</dt> <dd>

<span data-ttu-id="c39c4-110">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c39c4-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="c39c4-111">**DestinationIP**</span><span class="sxs-lookup"><span data-stu-id="c39c4-111">**DestinationIP**</span></span>
</dt> <dd>

<span data-ttu-id="c39c4-112">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c39c4-112">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="c39c4-113">**dwSourceport**</span><span class="sxs-lookup"><span data-stu-id="c39c4-113">**dwSourceport**</span></span>
</dt> <dd>

<span data-ttu-id="c39c4-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c39c4-114">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="c39c4-115">**dwDestinationport**</span><span class="sxs-lookup"><span data-stu-id="c39c4-115">**dwDestinationport**</span></span>
</dt> <dd>

<span data-ttu-id="c39c4-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c39c4-116">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="c39c4-117">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="c39c4-117">**Protocol**</span></span>
</dt> <dd>

<span data-ttu-id="c39c4-118">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c39c4-118">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="c39c4-119">**Link**</span><span class="sxs-lookup"><span data-stu-id="c39c4-119">**Link**</span></span>
</dt> <dd>

<span data-ttu-id="c39c4-120">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c39c4-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

<span data-ttu-id="c39c4-121"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c39c4-121"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c39c4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c39c4-122">Requirements</span></span>



| <span data-ttu-id="c39c4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c39c4-123">Requirement</span></span> | <span data-ttu-id="c39c4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c39c4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c39c4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c39c4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c39c4-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c39c4-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c39c4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c39c4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c39c4-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c39c4-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c39c4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c39c4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c39c4-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c39c4-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





