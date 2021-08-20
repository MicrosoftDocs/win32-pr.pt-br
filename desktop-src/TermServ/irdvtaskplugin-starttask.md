---
title: Método IRDVTaskPlugin StartTask
description: Chamado para iniciar a tarefa de atualização na máquina virtual.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método StartTask
- Método StartTask Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, método StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e0bb9104ee1bbd3f0f6c2e8cc04b691205f2e40cb2221b79b5e9f251492a3a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129253"
---
# <a name="irdvtaskpluginstarttask-method"></a>Método IRDVTaskPlugin:: StartTask

Chamado para iniciar a tarefa de atualização na máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Rótulo* \[ do no\]
</dt> <dd>

O rótulo da tarefa. Esse é o rótulo que foi passado para o agente de gatilho no método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Identificador* \[ do no\]
</dt> <dd>

O identificador da tarefa. Esse é o identificador que foi passado para o agente de gatilho no método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Contexto* \[ do no\]
</dt> <dd>

Dados opcionais para a tarefa. Esses são os dados que foram passados para o agente de gatilho no método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





