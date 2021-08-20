---
title: Enumeração de BITS_JOB_PROPERTY_ID (Deliveryoptimization. h)
description: A enumeração BITS_JOB_PROPERTY_ID especifica a ID da propriedade para o trabalho do. Essa enumeração é usada na União de BITS_JOB_PROPERTY_VALUE para determinar o tipo de valor contido na União.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- Enumeração de BITS_JOB_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 803e776bd635cd600bf664354dda8703d224dffcd63ea751919875a6ea69233d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047144"
---
# <a name="bits_job_property_id-enumeration"></a>Enumeração de BITS_JOB_PROPERTY_ID

A enumeração **BITS_JOB_PROPERTY_ID** especifica a ID da propriedade para o trabalho do. Essa enumeração é usada na União de [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) para determinar o tipo de valor contido na União.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**
</dt> <dd>

A ID usada para controlar o [comportamento de transferência](https://www.bing.com/search?q=control+transfer+behavior) por celular e/ou redes semelhantes. Essa propriedade pode ser alterada enquanto uma transferência está em andamento. os novos sinalizadores de custo entrarão em vigor imediatamente.

Essa propriedade usa o campo **Dword** **BITS_JOB_PROPERTY_VALUE** s.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**
</dt> <dd>

A ID usada para [registrar um retorno de chamada com](https://www.bing.com/search?q=register+a+COM+callback) pelo CLSID para receber notificações sobre o progresso e a conclusão de um trabalho do. O CLSID deve se referir a uma classe associada a um servidor COM fora do processo registrado. Ele também pode ser definido como **GUID_NULL** para limpar um CLSID de notificação definido anteriormente.

Essa propriedade usa o campo **CLsID** **BITS_JOB_PROPERTY_VALUE** s.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**
</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**
</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**
</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**
</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**
</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**
</dt> <dd>

Sem suporte.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> <dt>

[**IBackgroundCopyJob5:: SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[**IBackgroundCopyJob5:: GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





