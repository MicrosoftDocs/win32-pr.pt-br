---
title: Estrutura de MPTHREAT_DATA (MpClient. h)
description: Dados de notificação passados devido a uma detecção de ameaças ou modificação.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_DATA
- Ponteiro de estrutura de PMPTHREAT_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787665"
---
# <a name="mpthreat_data-structure"></a><span data-ttu-id="0be05-105">\_Estrutura de dados MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="0be05-105">MPTHREAT\_DATA structure</span></span>

<span data-ttu-id="0be05-106">Dados de notificação passados devido a uma detecção de ameaças ou modificação.</span><span class="sxs-lookup"><span data-stu-id="0be05-106">Notification data passed due to threat detection or modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be05-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0be05-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a><span data-ttu-id="0be05-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0be05-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0be05-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="0be05-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="0be05-110">Tipo: **\_ ID de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="0be05-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="0be05-111">Identificador de ameaça.</span><span class="sxs-lookup"><span data-stu-id="0be05-111">Threat identifier.</span></span> <span data-ttu-id="0be05-112">O bit superior é definido para identificar ameaças relacionadas ao antivírus.</span><span class="sxs-lookup"><span data-stu-id="0be05-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="0be05-113">**dwSessionID**</span><span class="sxs-lookup"><span data-stu-id="0be05-113">**dwSessionID**</span></span>
</dt> <dd>

<span data-ttu-id="0be05-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0be05-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0be05-115">Sessão associada à ameaça.</span><span class="sxs-lookup"><span data-stu-id="0be05-115">Session associated with the threat.</span></span> <span data-ttu-id="0be05-116">Defina como-1 se nenhuma informação específica de sessão estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="0be05-116">Set to -1 if no session specific information is available.</span></span>

</dd> <dt>

<span data-ttu-id="0be05-117">**Threataction**</span><span class="sxs-lookup"><span data-stu-id="0be05-117">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="0be05-118">Tipo: **[ **\_ ação MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="0be05-118">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0be05-119">Ação de ameaça tentada para a **\_ limpeza de ameaça mpnotify \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha na limpeza de ameaças** .</span><span class="sxs-lookup"><span data-stu-id="0be05-119">Threat action tried for the **MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**/**MPNOTIFY\_THREAT\_CLEAN\_FAILED** events.</span></span>

</dd> <dt>

<span data-ttu-id="0be05-120">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="0be05-120">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="0be05-121">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0be05-121">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0be05-122">Status ou ações adicionais associadas à ação executada.</span><span class="sxs-lookup"><span data-stu-id="0be05-122">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="0be05-123">Essa é uma combinação de sinalizadores de bit [**do \_ sinalizador MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="0be05-123">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0be05-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be05-124">Requirements</span></span>



| <span data-ttu-id="0be05-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be05-125">Requirement</span></span> | <span data-ttu-id="0be05-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0be05-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0be05-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be05-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0be05-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0be05-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0be05-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be05-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0be05-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0be05-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0be05-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be05-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0be05-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be05-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be05-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0be05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be05-134">**\_sinalizador MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="0be05-134">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="0be05-135">**\_ação MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="0be05-135">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





