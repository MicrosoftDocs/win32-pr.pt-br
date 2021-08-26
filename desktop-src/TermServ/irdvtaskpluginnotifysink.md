---
title: Interface IRDVTaskPluginNotifySink
description: A interface IRDVTaskPluginNotifySink é usada pelo agente de tarefa para se comunicar com o agente de gatilho.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Interface IRDVTaskPluginNotifySink Serviços de Área de Trabalho Remota
- Interface IRDVTaskPluginNotifySink Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88692175fedbad4faf5b2755ce92897cff25fe9d588e6fb446d8174407aa6b5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072386"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Interface IRDVTaskPluginNotifySink

A interface **IRDVTaskPluginNotifySink** é usada pelo agente de tarefa para se comunicar com o agente de gatilho. Um ponteiro para essa interface é passado para o agente de tarefa [**no método IRDVTaskPlugin::Initialize.**](irdvtaskplugin-initialize.md)

## <a name="members"></a>Membros

A interface **IRDVTaskPluginNotifySink** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPluginNotifySink** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IRDVTaskPluginNotifySink** tem esses métodos.



| Método                                                                  | Descrição                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Chamado pelo agente de tarefa para excluir uma tarefa agendada.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Usado para notificar o agente de gatilho de que o estado de uma tarefa foi alterado.<br/> |
| [**OnTerminated**](irdvtaskpluginnotifysink-onterminated.md)           | Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.<br/>  |
| [**Scheduletask**](irdvtaskpluginnotifysink-scheduletask.md)           | Chamado pelo agente de tarefa para agendar uma tarefa.<br/>                           |



 

## <a name="remarks"></a>Comentários

Embora essa interface tenha suporte nos sistemas operacionais identificados nos Requisitos abaixo, ela só será usada se a máquina virtual estiver hospedada no Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



 

