---
description: Essa classe é a classe pai para eventos de rastreamento de pilha.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Classe StackWalk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967418"
---
# <a name="stackwalk-class"></a>Classe StackWalk

Essa classe é a classe pai para eventos de rastreamento de pilha.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **StackWalk** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar o rastreamento de pilha de eventos de kernel, chame a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e especifique os eventos de kernel e os tipos para os quais você deseja capturar o rastreamento de pilha. Para habilitar o rastreamento de pilha para outros eventos, defina o membro **preaptoproperty** de [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) para **evento \_ habilitar \_ rastreamento de \_ pilha \_ de propriedades**.

Use o seguinte tipo de evento para identificar o evento real ao consumir eventos.



| Tipo de evento           | Descrição                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Valor do tipo de evento, 32 | Evento de rastreamento de pilha. A classe MOF do [**\_ evento StackWalk**](stackwalk-event.md) define os dados do evento para esse evento. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 
