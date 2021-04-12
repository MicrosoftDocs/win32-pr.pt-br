---
title: Enumeração de BG_JOB_TYPE (Deliveryoptimization. h)
description: A enumeração BG_JOB_TYPE define valores constantes que especificam o tipo de trabalho de transferência, como download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Enumeração de BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454965"
---
# <a name="bg_job_type-enumeration"></a>Enumeração de BG_JOB_TYPE

A enumeração **BG_JOB_TYPE** define valores constantes que especificam o tipo de trabalho de transferência, como download.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**
</dt> <dd>

Especifica que o trabalho baixa arquivos para o cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob:: GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





