---
title: Interface IReconcileInitiator
description: Expõe métodos que fornecem ao porta-arquivos reconciliador o meio para notificar o iniciador sobre seu progresso, definir um objeto de encerramento e solicitar uma determinada versão de um documento. O iniciador é responsável por implementar essa interface.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Recursos do ambiente Windows herdado da interface IReconcileInitiator
- Recursos do ambiente Windows herdado da interface IReconcileInitiator, descritos
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
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644674"
---
# <a name="ireconcileinitiator-interface"></a>Interface IReconcileInitiator

Expõe métodos que fornecem ao porta-arquivos reconciliador o meio para notificar o iniciador sobre seu progresso, definir um objeto de encerramento e solicitar uma determinada versão de um documento. O iniciador é responsável por implementar essa interface.

## <a name="members"></a>Membros

A interface **IReconcileInitiator** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReconcileInitiator** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IReconcileInitiator** tem esses métodos.



| Método                                                                 | Descrição                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Define o objeto por meio do qual o iniciador pode finalizar uma reconciliação de forma assíncrona. Um porta-arquivos reconciliador normalmente define esse objeto para reconciliações que são demoradas ou envolvem a interação do usuário. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Indica a quantidade de progresso que o porta-arquivos Reconciler fez para concluir a reconciliação. O valor é uma fração e é calculado como o quociente dos parâmetros *ulProgress* e *ulProgressMax* . Os reconciliadores devem chamar esse método periodicamente durante o processo de reconciliação. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,0 ou posterior)</dt> </dl> |



 

