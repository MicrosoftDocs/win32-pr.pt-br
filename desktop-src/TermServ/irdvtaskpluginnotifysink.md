---
title: Interface IRDVTaskPluginNotifySink
description: A interface IRDVTaskPluginNotifySink é usada pelo agente de tarefa para se comunicar com o agente de gatilho.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota da interface IRDVTaskPluginNotifySink, descrita
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644792"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Interface IRDVTaskPluginNotifySink

A interface **IRDVTaskPluginNotifySink** é usada pelo agente de tarefa para se comunicar com o agente de gatilho. Um ponteiro para essa interface é passado para o agente de tarefa no método [**IRDVTaskPlugin:: Initialize**](irdvtaskplugin-initialize.md) .

## <a name="members"></a>Membros

A interface **IRDVTaskPluginNotifySink** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPluginNotifySink** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IRDVTaskPluginNotifySink** tem esses métodos.



| Método                                                                  | Descrição                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Chamado pelo agente de tarefa para excluir uma tarefa agendada.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Usado para notificar o agente de disparo de que o estado de uma tarefa foi alterado.<br/> |
| [**Onterminado**](irdvtaskpluginnotifysink-onterminated.md)           | Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.<br/>  |
| [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md)           | Chamado pelo agente de tarefa para agendar uma tarefa.<br/>                           |



 

## <a name="remarks"></a>Comentários

Embora essa interface tenha suporte nos sistemas operacionais identificados nos requisitos abaixo, ela só será usada se a máquina virtual estiver hospedada no Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



 

