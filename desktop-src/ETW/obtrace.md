---
description: Representa a classe pai da qual todas as classes de rastreamento de eventos do Gerenciador de objetos são derivadas.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Classe ObTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662542"
---
# <a name="obtrace-class"></a>Classe ObTrace

Representa a classe pai da qual todas as classes de rastreamento de eventos do Gerenciador de objetos são derivadas.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **ObTrace** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar o rastreamento de eventos do Gerenciador de objetos, chame a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) com o parâmetro *InformationClass* igual ao valor de enumeração de [**classe de \_ informações \_ de rastreamento**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** e o membro **EnableFlags** da estrutura de [**\_ \_ Propriedades do rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) igual ao **\_ \_ identificador de OB perf** (0x80000040).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 
