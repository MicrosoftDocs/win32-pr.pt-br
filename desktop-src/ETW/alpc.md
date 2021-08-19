---
description: Essa classe é a classe pai para eventos avançados de chamada de procedimento local. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: Classe ALPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 435b55c44f06b6be062653a45e14a1a890e026371d8bd8e649c87ce3542118c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070286"
---
# <a name="alpc-class"></a>Classe ALPC

Essa classe é a classe pai para eventos avançados de chamada de procedimento local.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **ALPC** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de chamada de procedimento locais avançados em uma sessão de log do kernel NT, especifique o sinalizador **ALPC do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos ALPC chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ALPCGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os tipos de evento a seguir para identificar o evento ALPC real ao consumir eventos.



| Tipo de evento           | Descrição                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor do tipo de evento, 33 | Enviar evento de mensagem. A classe do MOF de [**\_ envio de \_ mensagem do ALPC**](alpc-send-message.md) define os dados do evento para esse evento.                           |
| Valor do tipo de evento, 34 | Receber evento de mensagem. A classe de [**\_ \_ mensagem MOF de recebimento ALPC**](alpc-receive-message.md) define os dados do evento para esse evento.                  |
| Valor do tipo de evento, 35 | Aguarde o evento de resposta. A classe de [**\_ aguardar espera \_ por \_ resposta**](alpc-wait-for-reply.md) do MOF define os dados do evento para esse evento.                    |
| Valor do tipo de evento, 36 | Aguarde o evento de nova mensagem. A classe de [**\_ espera de aguardar \_ \_ nova \_ mensagem**](alpc-wait-for-new-message.md) do o MOF define os dados do evento para esse evento. |
| Valor do tipo de evento, 37 | Interromper evento de espera. A classe MOF de [**\_ desesperação ALPC**](alpc-unwait.md) define os dados do evento para esse evento.                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

