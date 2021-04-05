---
title: Enumeração MPSOURCE (MpClient. h)
description: Categoria possível de origem.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Recursos do ambiente Windows herdado de enumeração MPSOURCE
- Ponteiro de enumeração PMPSOURCE recursos de ambiente do Windows herdados
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918715"
---
# <a name="mpsource-enumeration"></a><span data-ttu-id="38625-105">Enumeração MPSOURCE</span><span class="sxs-lookup"><span data-stu-id="38625-105">MPSOURCE enumeration</span></span>

<span data-ttu-id="38625-106">Categoria possível de origem.</span><span class="sxs-lookup"><span data-stu-id="38625-106">Possible category of source.</span></span>

## <a name="syntax"></a><span data-ttu-id="38625-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="38625-107">Syntax</span></span>


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a><span data-ttu-id="38625-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="38625-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="38625-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="38625-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="38625-110">Fonte desconhecida.</span><span class="sxs-lookup"><span data-stu-id="38625-110">Source unknown.</span></span>

</dd> <dt>

<span data-ttu-id="38625-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**\_usuário MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="38625-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**MPSOURCE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="38625-112">Iniciado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="38625-112">User initiated.</span></span>

</dd> <dt>

<span data-ttu-id="38625-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**\_sistema MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="38625-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**MPSOURCE\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="38625-114">iniciado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="38625-114">system initiated.</span></span>

</dd> <dt>

<span data-ttu-id="38625-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE em \_ tempo real**</span><span class="sxs-lookup"><span data-stu-id="38625-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE\_REALTIME**</span></span>
</dt> <dd>

<span data-ttu-id="38625-116">Componente em tempo real iniciado.</span><span class="sxs-lookup"><span data-stu-id="38625-116">Realtime component initiated.</span></span>

</dd> <dt>

<span data-ttu-id="38625-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE \_ IOAV**</span><span class="sxs-lookup"><span data-stu-id="38625-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE\_IOAV**</span></span>
</dt> <dd>

<span data-ttu-id="38625-118">Downloads do IE e anexos do Outlook Express iniciados.</span><span class="sxs-lookup"><span data-stu-id="38625-118">IE Downloads and Outlook Express Attachments initiated.</span></span>

</dd> <dt>

<span data-ttu-id="38625-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="38625-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="38625-120">Sistema de inspeção de rede.</span><span class="sxs-lookup"><span data-stu-id="38625-120">Network inspection system.</span></span>

</dd> <dt>

<span data-ttu-id="38625-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**\_BHO MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="38625-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE\_BHO**</span></span>
</dt> <dd>

<span data-ttu-id="38625-122">BHO-script da Web (preterido).</span><span class="sxs-lookup"><span data-stu-id="38625-122">BHO - web script (deprecated).</span></span>

</dd> <dt>

<span data-ttu-id="38625-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE \_ IEPROTECT**</span><span class="sxs-lookup"><span data-stu-id="38625-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE\_IEPROTECT**</span></span>
</dt> <dd>

<span data-ttu-id="38625-124">IE-IExtensionValidation.</span><span class="sxs-lookup"><span data-stu-id="38625-124">IE - IExtensionValidation.</span></span>

</dd> <dt>

<span data-ttu-id="38625-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE \_ Elam**</span><span class="sxs-lookup"><span data-stu-id="38625-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE\_ELAM**</span></span>
</dt> <dd>

<span data-ttu-id="38625-126">ELAM</span><span class="sxs-lookup"><span data-stu-id="38625-126">ELAM</span></span>

</dd> <dt>

<span data-ttu-id="38625-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**\_atestado local de MPSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="38625-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**MPSOURCE\_LOCAL\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="38625-128">Atestado local.</span><span class="sxs-lookup"><span data-stu-id="38625-128">Local attestation.</span></span>

</dd> <dt>

<span data-ttu-id="38625-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**\_atestado remoto \_ MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="38625-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**MPSOURCE\_REMOTE\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="38625-130">Atestado remoto.</span><span class="sxs-lookup"><span data-stu-id="38625-130">Remote attestation.</span></span>

</dd> <dt>

<span data-ttu-id="38625-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE \_ AMSI**</span><span class="sxs-lookup"><span data-stu-id="38625-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE\_AMSI**</span></span>
</dt> <dd>

<span data-ttu-id="38625-132">AMSI</span><span class="sxs-lookup"><span data-stu-id="38625-132">AMSI</span></span>

</dd> <dt>

<span data-ttu-id="38625-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**origem do MP \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="38625-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP\_SOURCE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="38625-134">Valor máximo possível.</span><span class="sxs-lookup"><span data-stu-id="38625-134">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38625-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38625-135">Requirements</span></span>



| <span data-ttu-id="38625-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="38625-136">Requirement</span></span> | <span data-ttu-id="38625-137">Valor</span><span class="sxs-lookup"><span data-stu-id="38625-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38625-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38625-138">Minimum supported client</span></span><br/> | <span data-ttu-id="38625-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="38625-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="38625-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38625-140">Minimum supported server</span></span><br/> | <span data-ttu-id="38625-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="38625-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38625-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38625-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="38625-143"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="38625-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





