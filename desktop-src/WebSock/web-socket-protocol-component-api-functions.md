---
title: Funções de API do componente de protocolo WebSocket
description: A API de Componente de Protocolo WebSocket define essas funções.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d88a4ef8eb9caa0e409d0ded60b6dffd2717dc74d1b2cdddeb08ee6d9de08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330334"
---
# <a name="websocket-protocol-component-api-functions"></a>Funções de API do componente de protocolo WebSocket

A API de Componente de Protocolo WebSocket define essas funções.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                             | Descrição                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WebSocketAbortHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | anula um alça de sessão WebSocket criado por [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) ou [**WebSocketCreateServerHandle.**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)<br/>   |
| [**WebSocketBeginClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | inicia o handshake do lado do cliente.<br/>                                                                                                                                                                |
| [**WebSocketBeginServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | inicia o handshake do lado do servidor.<br/>                                                                                                                                                                |
| [**WebSocketCompleteAction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | conclui uma ação iniciada por [**WebSocketGetAction.**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction)<br/>                                                                                                             |
| [**WebSocketCreateClientHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | cria um alça de sessão WebSocket do lado do cliente.<br/>                                                                                                                                                  |
| [**WebSocketCreateServerHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | cria um alça de sessão WebSocket do lado do servidor.<br/>                                                                                                                                                  |
| [**WebSocketDeleteHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | exclui um alça de sessão WebSocket criado por [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) ou [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>  |
| [**WebSocketEndClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | conclui o handshake do lado do cliente.<br/>                                                                                                                                                             |
| [**WebSocketEndServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | conclui o handshake do lado do servidor.<br/>                                                                                                                                                             |
| [**WebSocketGetAction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | retorna uma ação de uma chamada para [**WebSocketSend**](/windows/desktop/api/websocket/nf-websocket-websocketsend), [**WebSocketReceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) ou [**WebSocketCompleteAction**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction).<br/> |
| [**WebSocketGetGlobalProperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | obtém uma única propriedade WebSocket.<br/>                                                                                                                                                                |
| [**WebSocketReceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | adiciona uma operação de recebimento à fila de operação do componente de protocolo.<br/>                                                                                                                              |
| [**WebSocketSend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | adiciona uma operação de envio à fila de operação do componente de protocolo.<br/>                                                                                                                                 |



 

 

