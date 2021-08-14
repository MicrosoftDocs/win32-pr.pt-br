---
title: Interface IBackgroundCopyError (Deliveryoptimization.h)
description: Use a interface IBackgroundCopyError para determinar a causa de um erro e se o processo de transferência pode continuar.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interface IBackgroundCopyError
- Interface IBackgroundCopyError, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73e4dd3a74529bb95d1e80597579d6a0aa5885302b9b26d851dc341c9cd1a9a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101648"
---
# <a name="ibackgroundcopyerror-interface"></a>Interface IBackgroundCopyError

Use a interface **IBackgroundCopyError** para determinar a causa de um erro e se o processo de transferência pode continuar.

DO cria um objeto de erro somente quando o estado do trabalho é BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR. DO não cria um objeto de erro quando um método de interface **IBackgroundCopyXXXX** falha. O objeto de erro está disponível até que DO comece a transferir dados (o estado do trabalho muda para BG_JOB_STATE_TRANSFERRING) para o trabalho.

Para obter um **objeto IBackgroundCopyError,** chame o [**método IBackgroundCopyJob::GetError.**](ibackgroundcopyjob-geterror.md)

## <a name="members"></a>Membros

A interface **IBackgroundCopyError** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyError** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyError** tem esses métodos.



| Método                                                   | Descrição                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Geterror**](ibackgroundcopyerror-geterror-method.md) | Recupera o código de erro e identifica o contexto no qual o erro ocorreu.<br/> |
| [**Getfile**](ibackgroundcopyerror-getfile-method.md)   | Recupera um ponteiro de interface para o objeto de arquivo associado ao erro.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

