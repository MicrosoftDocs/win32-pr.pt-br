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
# <a name="adsi-print-job-status-constants"></a>Constantes de status do trabalho de impressão ADSI

As constantes a seguir são usadas com a propriedade [**IADsPrintJobOperations. status**](iadsprintjoboperations-property-methods.md) para indicar o status de um trabalho de impressão.

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**trabalho do ADS em \_ \_ pausa**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



O trabalho de impressão está em pausa.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_erro de trabalho do ADS \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Ocorreu um erro.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_exclusão de trabalhos do ADS \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



O trabalho de impressão está sendo excluído.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_spool de trabalhos do ADS \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



O trabalho de impressão está sendo colocado no spool.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_impressão de trabalhos do ADS \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



O trabalho de impressão está sendo impresso.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**trabalho do ADS \_ \_ offline**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



A impressora está offline.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_papel de trabalho do ADS \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



A impressora está sem papel.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**trabalho do ADS \_ \_ impresso**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



O trabalho de impressão foi impresso.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**trabalho do ADS \_ \_ excluído**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



O trabalho de impressão foi excluído.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Adssts. h</dt> </dl> |



 

 





