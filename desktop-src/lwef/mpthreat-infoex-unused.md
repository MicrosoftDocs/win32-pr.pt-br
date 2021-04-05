---
title: Estrutura de MPTHREAT_INFOEX_UNUSED (MpClient. h)
description: Estrutura fictícia para ameaças de tipo de modificação sem comportamento.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_INFOEX_UNUSED
- Ponteiro de estrutura de PMPTHREAT_INFOEX_UNUSED recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085841"
---
# <a name="mpthreat_infoex_unused-structure"></a><span data-ttu-id="eb3f4-105">\_ \_ Estrutura não utilizada do MPTHREAT INFOEX</span><span class="sxs-lookup"><span data-stu-id="eb3f4-105">MPTHREAT\_INFOEX\_UNUSED structure</span></span>

<span data-ttu-id="eb3f4-106">Estrutura fictícia para ameaças de tipo de modificação sem comportamento.</span><span class="sxs-lookup"><span data-stu-id="eb3f4-106">Dummy structure for non-behavior modification type threats.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3f4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb3f4-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="eb3f4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="eb3f4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb3f4-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="eb3f4-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="eb3f4-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="eb3f4-110">Type: **DWORD**</span></span>

<span data-ttu-id="eb3f4-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eb3f4-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="eb3f4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb3f4-112">Requirements</span></span>



| <span data-ttu-id="eb3f4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb3f4-113">Requirement</span></span> | <span data-ttu-id="eb3f4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="eb3f4-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3f4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb3f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="eb3f4-116">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eb3f4-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="eb3f4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb3f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="eb3f4-118">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eb3f4-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb3f4-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb3f4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb3f4-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb3f4-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





