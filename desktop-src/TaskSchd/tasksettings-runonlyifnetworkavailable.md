---
title: Propriedade TaskSettings. RunOnlyIfNetworkAvailable
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Agendador de Tarefas da propriedade RunOnlyIfNetworkAvailable
- Propriedade RunOnlyIfNetworkAvailable Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824652"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>Propriedade TaskSettings. RunOnlyIfNetworkAvailable

Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a propriedade indicará que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível. O padrão é False.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





