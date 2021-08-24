---
title: Método Cancel de IBackgroundCopyJob (Deliveryoptimization.h)
description: Exclui o trabalho da fila de transferência e remove arquivos temporários relacionados do cliente (downloads) e do servidor (uploads).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Método Cancel
- Método Cancel, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c30fa0d7dcc4aa6137fbfef8d40a91d4839bc59d624c8ba2c942fb6c2041fccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635846"
---
# <a name="ibackgroundcopyjobcancel-method"></a>Método IBackgroundCopyJob::Cancel

Exclui o trabalho da fila de transferência e remove arquivos temporários relacionados do cliente (downloads) e do servidor (uploads).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                                          | Descrição                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | O trabalho foi cancelado com êxito.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Não é possível cancelar um trabalho cujo estado BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentários

Você pode cancelar um trabalho a qualquer momento; no entanto, o trabalho não pode ser recuperado depois que ele é cancelado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





