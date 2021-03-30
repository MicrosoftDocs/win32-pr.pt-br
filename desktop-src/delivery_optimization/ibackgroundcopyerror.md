---
title: Interface IBackgroundCopyError (Deliveryoptimization. h)
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
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455031"
---
# <a name="ibackgroundcopyerror-interface"></a>Interface IBackgroundCopyError

Use a interface **IBackgroundCopyError** para determinar a causa de um erro e se o processo de transferência pode continuar.

O cria um objeto de erro somente quando o estado do trabalho é BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR. Não cria um objeto de erro quando um método de interface **IBackgroundCopyXXXX** falha. O objeto de erro estará disponível até que o comece a transferir dados (o estado do trabalho é alterado para BG_JOB_STATE_TRANSFERRING) para o trabalho.

Para obter um objeto **IBackgroundCopyError** , chame o método [**método ibackgroundcopyjob:: GetError**](ibackgroundcopyjob-geterror.md) .

## <a name="members"></a>Membros

A interface **IBackgroundCopyError** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyError** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyError** tem esses métodos.



| Método                                                   | Descrição                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Recupera o código de erro e identifica o contexto no qual ocorreu o erro.<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | Recupera um ponteiro de interface para o objeto de arquivo associado ao erro.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

