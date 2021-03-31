---
title: Método método ibackgroundcopyjob Cancel (Deliveryoptimization. h)
description: Exclui o trabalho da fila de transferência e remove arquivos temporários relacionados do cliente (downloads) e do servidor (uploads).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Método Cancel
- Método Cancel, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método Cancel
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
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824350"
---
# <a name="ibackgroundcopyjobcancel-method"></a>Método método ibackgroundcopyjob:: Cancel

Exclui o trabalho da fila de transferência e remove arquivos temporários relacionados do cliente (downloads) e do servidor (uploads).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                                          | Description                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | O trabalho foi cancelado com êxito.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Não é possível cancelar um trabalho cujo estado é BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentários

Você pode cancelar um trabalho a qualquer momento; no entanto, o trabalho não pode ser recuperado após ser cancelado.

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: concluir**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: retomar**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: suspender**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





