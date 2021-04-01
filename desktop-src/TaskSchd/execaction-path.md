---
title: Propriedade execaction. Path
description: Para scripts, Obtém ou define o caminho para um arquivo executável.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Agendador de Tarefas de propriedade de caminho
- Propriedade Path Agendador de Tarefas, objeto Execaction
- Agendador de Tarefas de objeto execaction, propriedade Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644489"
---
# <a name="execactionpath-property"></a>Propriedade execaction. Path

Para scripts, Obtém ou define o caminho para um arquivo executável.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Valor da propriedade

O caminho para o arquivo executável a ser executado pela ação.

## <a name="remarks"></a>Comentários

Essa ação executa uma operação de linha de comando. Por exemplo, a ação pode executar um script ou iniciar um executável.

Ao ler ou gravar XML, o caminho da operação de linha de comando é especificado no elemento [**Command**](taskschedulerschema-command-exectype-element.md) do esquema de Agendador de tarefas.

O caminho é verificado para certificar-se de que ele é válido quando a tarefa é registrada, não quando essa propriedade é definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Execaction**](execaction.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





