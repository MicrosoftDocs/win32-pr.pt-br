---
title: Método método ibackgroundcopyjob SetNotifyInterface (Deliveryoptimization. h)
description: Identifica a implementação da interface IBackgroundCopyCallback a ser feita. Use a interface IBackgroundCopyCallback para receber a notificação de eventos relacionados ao trabalho.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Método SetNotifyInterface
- Método SetNotifyInterface, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método SetNotifyInterface
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
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295772"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>Método método ibackgroundcopyjob:: SetNotifyInterface

Identifica a implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) a ser feita. Use a interface **IBackgroundCopyCallback** para receber a notificação de eventos relacionados ao trabalho.

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

Um ponteiro de interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Para remover o ponteiro de interface de retorno de chamada atual, defina esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | O ponteiro da interface de notificação foi definido com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método somente se você implementar a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Use o método **SetNotifyInterface** em conjunto com o método [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para especificar o tipo de notificação que você deseja receber.

A interface de notificação torna-se inválida quando o aplicativo é encerrado; Não mantém a interface de notificação. Como resultado, o processo de inicialização do aplicativo deve chamar o método **SetNotifyInterface** nesses trabalhos existentes para os quais você deseja receber a notificação. Se você precisar capturar informações de estado e de progresso ocorridas desde a última vez em que seu aplicativo foi executado, pesquise informações de estado e progresso durante a inicialização do aplicativo.

Somente o proprietário/criador do trabalho ou um administrador pode se registrar para notificações.

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





