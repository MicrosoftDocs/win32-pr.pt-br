---
title: Constantes de status do trabalho de impressão ADSI (Adssts. h)
description: As constantes a seguir são usadas com a propriedade IADsPrintJobOperations. status para indicar o status de um trabalho de impressão.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918895"
---
# <a name="adsi-print-job-status-constants"></a><span data-ttu-id="81970-103">Constantes de status do trabalho de impressão ADSI</span><span class="sxs-lookup"><span data-stu-id="81970-103">ADSI Print Job Status Constants</span></span>

<span data-ttu-id="81970-104">As constantes a seguir são usadas com a propriedade [**IADsPrintJobOperations. status**](iadsprintjoboperations-property-methods.md) para indicar o status de um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="81970-104">The following constants are used with the [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) property to indicate the status of a print job.</span></span>

<dl> <dt>

<span data-ttu-id="81970-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**trabalho do ADS em \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="81970-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS\_JOB\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="81970-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="81970-107">O trabalho de impressão está em pausa.</span><span class="sxs-lookup"><span data-stu-id="81970-107">The print job is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_erro de trabalho do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="81970-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS\_JOB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="81970-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="81970-110">Ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="81970-110">An error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_exclusão de trabalhos do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="81970-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ADS\_JOB\_DELETING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="81970-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="81970-113">O trabalho de impressão está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="81970-113">The print job is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_spool de trabalhos do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="81970-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS\_JOB\_SPOOLING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="81970-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="81970-116">O trabalho de impressão está sendo colocado no spool.</span><span class="sxs-lookup"><span data-stu-id="81970-116">The print job is being spooled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_impressão de trabalhos do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="81970-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS\_JOB\_PRINTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="81970-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="81970-119">O trabalho de impressão está sendo impresso.</span><span class="sxs-lookup"><span data-stu-id="81970-119">The print job is being printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**trabalho do ADS \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="81970-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS\_JOB\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-121">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="81970-121">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="81970-122">A impressora está offline.</span><span class="sxs-lookup"><span data-stu-id="81970-122">The printer is offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_papel de trabalho do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="81970-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS\_JOB\_PAPEROUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-124">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="81970-124">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="81970-125">A impressora está sem papel.</span><span class="sxs-lookup"><span data-stu-id="81970-125">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**trabalho do ADS \_ \_ impresso**</span><span class="sxs-lookup"><span data-stu-id="81970-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS\_JOB\_PRINTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-127">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="81970-127">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="81970-128">O trabalho de impressão foi impresso.</span><span class="sxs-lookup"><span data-stu-id="81970-128">The print job has been printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81970-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**trabalho do ADS \_ \_ excluído**</span><span class="sxs-lookup"><span data-stu-id="81970-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS\_JOB\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81970-130">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="81970-130">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="81970-131">O trabalho de impressão foi excluído.</span><span class="sxs-lookup"><span data-stu-id="81970-131">The print job has been deleted.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81970-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81970-132">Requirements</span></span>



| <span data-ttu-id="81970-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="81970-133">Requirement</span></span> | <span data-ttu-id="81970-134">Valor</span><span class="sxs-lookup"><span data-stu-id="81970-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="81970-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81970-135">Minimum supported client</span></span><br/> | <span data-ttu-id="81970-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81970-136">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="81970-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81970-137">Minimum supported server</span></span><br/> | <span data-ttu-id="81970-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81970-138">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="81970-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81970-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="81970-140"><dt>Adssts. h</dt></span><span class="sxs-lookup"><span data-stu-id="81970-140"><dt>Adssts.h</dt></span></span> </dl> |



 

 





