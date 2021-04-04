---
title: Método método ibackgroundcopyjob GetType (Deliveryoptimization. h)
description: Recupera o tipo de transferência que está sendo executada, como um download de arquivo ou upload.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- Método GetType
- Método GetType, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009013"
---
# <a name="ibackgroundcopyjobgettype-method"></a>Método método ibackgroundcopyjob:: GetType

Recupera o tipo de transferência que está sendo executada, como um download de arquivo ou upload.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJobType* \[ fora\]
</dt> <dd>

Tipo de transferência sendo executada. Para obter uma lista de tipos de transferência, consulte a enumeração [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | O tipo de transferência foi recuperado com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Especifique o tipo de transferência ao criar o trabalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_TYPE**](bg-job-type.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





