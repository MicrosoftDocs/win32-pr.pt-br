---
title: Método IRDVTaskPluginNotifySink ScheduleTask
description: Chamado pelo agente de tarefa para agendar uma tarefa.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ScheduleTask
- Método ScheduleTask Serviços de Área de Trabalho Remota, interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink, método ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824761"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>Método IRDVTaskPluginNotifySink:: ScheduleTask

Chamado pelo agente de tarefa para agendar uma tarefa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ftStartTime* \[ no\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

A hora de início da tarefa mais antiga, em UTC.

</dd> <dt>

*ftEndTime* \[ no\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

A hora de término da tarefa, em UTC. Passe um [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) definido para todos os zeros se nenhuma hora de término for especificada.

</dd> <dt>

*ftDeadline* \[ no\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

A data limite da tarefa, em UTC. Isso é usado para definir a prioridade para várias tarefas que estão dentro de sua janela inicial. Se mais de uma tarefa deve ser iniciada, aquela com o prazo mais antigo será iniciada primeiro.

</dd> <dt>

*bstrLabel* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O rótulo da tarefa. Isso é passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*bstrIdentifier* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O identificador da tarefa. Isso é passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*saContext* \[ no\]
</dt> <dd>

Tipo: **SafeArray (Byte)**

Dados opcionais para a tarefa. Isso é passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

