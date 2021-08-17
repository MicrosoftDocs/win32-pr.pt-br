---
description: Essa classe é a classe pai para eventos de e/s de divisão. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Classe SplitIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0268c3dfa778eb8694a81f57b9212b68bd6674e6c7de6324cdc297550745b2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069716"
---
# <a name="splitio-class"></a>Classe SplitIo

Essa classe é a classe pai para eventos de e/s de divisão.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **SplitIo** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de e/s de divisão em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ e/s de divisão do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de e/s de divisão chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**SplitIoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use o seguinte tipo de evento para identificar o evento real ao consumir eventos.



| Tipo de evento           | Descrição                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Valor do tipo de evento, 32 | Dividir evento de e/s. A classe MOF [**SplitIo \_ info**](splitio-info.md) define os dados do evento para esse evento. |



 

Eventos de e/s de divisão indicam que as solicitações de e/s foram divididas em várias solicitações de e/s de disco devido ao hardware de disco de espelhamento subjacente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 
