---
title: Interface IReconcileInitiator
description: Expõe métodos que fornecem ao reconciliador os meios para notificar o iniciador de seu progresso, definir um objeto de encerramento e solicitar uma determinada versão de um documento. O iniciador é responsável por implementar essa interface.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Interface IReconcileInitiator Herdado Windows ambiente
- IReconcileInitiator interface Legacy Windows Environment Features , descrito
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff81862e5ff0b27b75f952749957e6559306257240f2a02aca5f34e3efc870cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749136"
---
# <a name="ireconcileinitiator-interface"></a>Interface IReconcileInitiator

Expõe métodos que fornecem ao reconciliador os meios para notificar o iniciador de seu progresso, definir um objeto de encerramento e solicitar uma determinada versão de um documento. O iniciador é responsável por implementar essa interface.

## <a name="members"></a>Membros

A interface **IReconcileInitiator** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IReconcileInitiator** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IReconcileInitiator** tem esses métodos.



| Método                                                                 | Descrição                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Define o objeto por meio do qual o iniciador pode encerrar uma reconciliação de forma assíncrona. Um reconciliador de pastas normalmente define esse objeto para reconciliação que são longas ou envolvem a interação do usuário. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Indica a quantidade de progresso que o reconciliador fez para concluir a reconciliação. O valor é uma fração e é calculado como o quociente dos parâmetros *ulProgress* e *ulProgressMax.* Os reconciliadores devem chamar esse método periodicamente durante o processo de reconciliação. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.0 ou posterior)</dt> </dl> |



 

