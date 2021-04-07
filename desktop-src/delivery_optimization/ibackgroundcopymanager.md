---
title: Interface IBackgroundCopyManager (Deliveryoptimization. h)
description: Cria trabalhos de transferência, recupera um objeto enumerador que contém os trabalhos na fila e recupera trabalhos individuais da fila.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918571"
---
# <a name="ibackgroundcopymanager-interface"></a>Interface IBackgroundCopyManager

Cria trabalhos de transferência, recupera um objeto enumerador que contém os trabalhos na fila e recupera trabalhos individuais da fila.

## <a name="members"></a>Membros

A interface **IBackgroundCopyManager** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyManager** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyManager** tem esses métodos.



| Método                                                | Descrição                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**CreateJob**](ibackgroundcopymanager-createjob.md) | Cria um trabalho de transferência.<br/>                   |
| [**GetJob**](ibackgroundcopymanager-getjob.md)       | Recupera um trabalho especificado da fila.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager é definido como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

