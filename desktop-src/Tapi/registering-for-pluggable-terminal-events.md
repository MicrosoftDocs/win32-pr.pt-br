---
description: O processo de registro de eventos ocorre quando o terminal é selecionado por um fluxo.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrando para eventos de terminal conectável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71993d597cbcba7c634068813eb14939539dc7e7d43cda0105e8cf9ee615a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060454"
---
# <a name="registering-for-pluggable-terminal-events"></a>Registrando para eventos de terminal conectável

O processo de registro de eventos ocorre quando o terminal é selecionado por um fluxo. Na implementação do aplicativo de terminal do método [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) , podemos usar a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) do terminal que foi anexado ao fluxo e chamar **QueryInterface** para localizar [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Se a chamada **QueryInterface** for realizada com sucesso, podemos chamar o método [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) . Para essa finalidade, devemos criar um objeto que implementa a interface [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) . Passamos essa interface como um parâmetro do método **RegisterSink** .

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

O terminal que implementa a chamada [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) armazenará a interface. O ponteiro será usado quando o terminal disparar um evento.

O coletor de eventos pode ter o registro cancelado usando [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
