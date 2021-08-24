---
title: Método IBackgroundCopyJob SetNotifyInterface (Deliveryoptimization.h)
description: Identifica sua implementação da interface IBackgroundCopyCallback para DO. Use a interface IBackgroundCopyCallback para receber notificação de eventos relacionados ao trabalho.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Método SetNotifyInterface
- Método SetNotifyInterface, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd54255d87ee3f15f87d692e06b7a503e773634ab4ec30c3f388388233aab2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793399"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>Método IBackgroundCopyJob::SetNotifyInterface

Identifica sua implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para DO. Use a interface **IBackgroundCopyCallback** para receber notificação de eventos relacionados ao trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNotifyInterface* 
</dt> <dd>

Um ponteiro de interface [**IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Para remover o ponteiro da interface de retorno de chamada atual, de definido esse parâmetro como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                              | Descrição                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | O ponteiro da interface de notificação foi definido com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método somente se você implementar a interface [**IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Use o **método SetNotifyInterface** em conjunto com o [**método SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para especificar o tipo de notificação que você deseja receber.

A interface de notificação se torna inválida quando o aplicativo é encerrado; DO não persiste a interface de notificação. Como resultado, o processo de inicialização do aplicativo deve chamar o método **SetNotifyInterface** nesses trabalhos existentes para os quais você deseja receber a notificação. Se você precisar capturar informações de estado e progresso que ocorreram desde a última vez que seu aplicativo foi executado, sondar informações de estado e progresso durante a inicialização do aplicativo.

Somente o proprietário/criador do trabalho ou um administrador pode se registrar para notificações.

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





