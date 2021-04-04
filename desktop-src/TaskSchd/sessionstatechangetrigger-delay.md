---
title: Propriedade SessionStateChangeTrigger. Delay
description: Para scripts, Obtém ou define um valor que indica por quanto tempo um atraso ocorre antes de uma tarefa ser iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto SessionStateChangeTrigger
- Agendador de Tarefas de objeto SessionStateChangeTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085318"
---
# <a name="sessionstatechangetriggerdelay-property"></a>Propriedade SessionStateChangeTrigger. Delay

Para scripts, Obtém ou define um valor que indica por quanto tempo um atraso ocorre antes de uma tarefa ser iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Valor da propriedade

O atraso que ocorre antes de uma tarefa ser iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





