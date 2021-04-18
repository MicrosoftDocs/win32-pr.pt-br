---
title: Interface IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implemente a interface IBackgroundCopyCallback para receber a notificação de que um trabalho foi concluído, foi modificado ou está com erro. Os clientes usam essa interface em vez de sondar o status do trabalho.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105798273"
---
# <a name="ibackgroundcopycallback-interface"></a>Interface IBackgroundCopyCallback

Implemente a interface **IBackgroundCopyCallback** para receber a notificação de que um trabalho foi concluído, foi modificado ou está com erro. Os clientes usam essa interface em vez de sondar o status do trabalho.

## <a name="members"></a>Membros

A interface **IBackgroundCopyCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyCallback** tem esses métodos.



| Método                                                                    | Descrição                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Chamado quando ocorre um erro.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Chamado quando um trabalho é modificado.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Chamado quando todos os arquivos no trabalho foram transferidos com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Para receber notificações, chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para especificar o ponteiro de interface para sua implementação de **IBackgroundCopyCallback** . Para especificar quais notificações você deseja receber, chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .

Chamará seus retornos de chamada, desde que o ponteiro de interface seja válido. A interface de notificação não é mais válida quando o aplicativo é encerrado; Não mantém a interface de notificação. Como resultado, o processo de inicialização do aplicativo deve chamar o método [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) nesses trabalhos existentes para os quais você deseja receber a notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

