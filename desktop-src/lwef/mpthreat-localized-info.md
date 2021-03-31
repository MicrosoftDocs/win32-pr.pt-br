---
title: Estrutura de MPTHREAT_LOCALIZED_INFO (MpClient. h)
description: Informações localizadas para uma ameaça.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_LOCALIZED_INFO
- Ponteiro de estrutura de PMPTHREAT_LOCALIZED_INFO recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369587"
---
# <a name="mpthreat_localized_info-structure"></a><span data-ttu-id="126f5-105">\_Estrutura de informações localizadas do MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="126f5-105">MPTHREAT\_LOCALIZED\_INFO structure</span></span>

<span data-ttu-id="126f5-106">Informações localizadas para uma ameaça.</span><span class="sxs-lookup"><span data-stu-id="126f5-106">Localized information for a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="126f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="126f5-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a><span data-ttu-id="126f5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="126f5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="126f5-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="126f5-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-110">Tipo: **\_ ID de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="126f5-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-111">Identificador de ameaça.</span><span class="sxs-lookup"><span data-stu-id="126f5-111">Threat identifier.</span></span> <span data-ttu-id="126f5-112">O bit superior é definido para identificar ameaças relacionadas ao antivírus.</span><span class="sxs-lookup"><span data-stu-id="126f5-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-113">**CategoryName**</span><span class="sxs-lookup"><span data-stu-id="126f5-113">**CategoryName**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-114">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-114">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-115">Classificação de ameaças, como um cavalo de Troia ou um keylogger.</span><span class="sxs-lookup"><span data-stu-id="126f5-115">Threat classification, such as a trojan or a keylogger.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-116">**CategoryDescription**</span><span class="sxs-lookup"><span data-stu-id="126f5-116">**CategoryDescription**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-117">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-118">Descrição da categoria de ameaça.</span><span class="sxs-lookup"><span data-stu-id="126f5-118">Description of threat category.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-119">**Gravidadename**</span><span class="sxs-lookup"><span data-stu-id="126f5-119">**SeverityName**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-120">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-121">Nível de severidade da ameaça, como grave ou moderado.</span><span class="sxs-lookup"><span data-stu-id="126f5-121">Threat severity level, such as severe or moderate.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-122">**SeverityDescription**</span><span class="sxs-lookup"><span data-stu-id="126f5-122">**SeverityDescription**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-123">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-123">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-124">Descrição do nível de severidade da ameaça.</span><span class="sxs-lookup"><span data-stu-id="126f5-124">Description of threat severity level.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-125">**ShortDescription**</span><span class="sxs-lookup"><span data-stu-id="126f5-125">**ShortDescription**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-126">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-126">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-127">Breve descrição da ameaça.</span><span class="sxs-lookup"><span data-stu-id="126f5-127">Short description of threat.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-128">**Defaultactionname;**</span><span class="sxs-lookup"><span data-stu-id="126f5-128">**DefaultActionName;**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-129">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-130">Nome da ação padrão, como remover ou colocar em quarentena, sugerido pelo mecanismo.</span><span class="sxs-lookup"><span data-stu-id="126f5-130">Name of default action, such as remove or quarantine, suggested by engine.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-131">**Aconselhamento**</span><span class="sxs-lookup"><span data-stu-id="126f5-131">**Advice**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-132">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-133">Conselhos para a ameaça específica.</span><span class="sxs-lookup"><span data-stu-id="126f5-133">Advice for the particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="126f5-134">**ThreatUrl**</span><span class="sxs-lookup"><span data-stu-id="126f5-134">**ThreatUrl**</span></span>
</dt> <dd>

<span data-ttu-id="126f5-135">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="126f5-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="126f5-136">Uma URL para uma página da Web que contém informações sobre a ameaça.</span><span class="sxs-lookup"><span data-stu-id="126f5-136">A URL to a webpage containing information about the threat.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="126f5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="126f5-137">Requirements</span></span>



| <span data-ttu-id="126f5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="126f5-138">Requirement</span></span> | <span data-ttu-id="126f5-139">Valor</span><span class="sxs-lookup"><span data-stu-id="126f5-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="126f5-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="126f5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="126f5-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="126f5-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="126f5-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="126f5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="126f5-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="126f5-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="126f5-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="126f5-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="126f5-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="126f5-145"><dt>MpClient.h</dt></span></span> </dl> |



 

 





