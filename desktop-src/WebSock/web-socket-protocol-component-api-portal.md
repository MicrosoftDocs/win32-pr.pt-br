---
title: API de componente de protocolo WebSocket
description: API de componente de protocolo WebSocket
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16290a7af5b5fea406e5f47c0db718d775e4d17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088814"
---
# <a name="websocket-protocol-component-api"></a>API de componente de protocolo WebSocket

## <a name="purpose"></a>Finalidade

A API do componente de protocolo WebSocket permite canais de comunicação assíncronas e bidirecionais sobre HTTP que funcionam entre intermediários de rede existentes. Com a API de componente de protocolo WebSocket, um cliente usa HTTP para se comunicar com um servidor e ambos os lados alternam para usando o protocolo subjacente em que o HTTP foi colocado em camadas (como TCP ou SSL). O objetivo é primeiro usar HTTP para atravessar os intermediários da rede e, em seguida, usar o canal TCP/SSL subjacente de ponta a ponta para comunicação de aplicativo bidirecional. O protocolo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] é definido na IETF, enquanto um W3CAPI de API JavaScript associado \[ [](https://dev.w3.org/html5/websockets/) \] é definido no W3C.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                          | Descrição                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Tipos de dados da API do componente de protocolo WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | A API do componente de protocolo WebSocket define esses tipos de dados.<br/>   |
| [Enumerações de API de componente de protocolo WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | A API do componente de protocolo WebSocket define essas enumerações.<br/> |
| [Funções da API do componente de protocolo WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | A API do componente de protocolo WebSocket define essas funções.<br/>    |
| [Estruturas de API de componente de protocolo WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | A API do componente de protocolo WebSocket define essas estruturas.<br/>   |



 

## <a name="developer-audience"></a>Público de desenvolvedores

A API do componente de protocolo WebSocket foi projetada para uso por programadores C/C++. É necessário ter familiaridade com a rede HTTP e do Windows.

> [!Note]  
> A maneira preferida de usar o protocolo WebSocket no Windows é por meio da API do Windows [http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) ou do [namespace Windows. Networking. Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API do componente de protocolo WebSocket requer o Windows 8 e versões posteriores do sistema operacional Windows. As APIs podem ser vinculadas dinamicamente por meio de websocket.dll.

> [!Note]  
> websocket.dll fornece suporte para cabeçalhos HTTP relacionados a Handshakes de cliente e de servidor, verifica os dados de handshake recebidos e analisa o fluxo de dados WebSocket. Ele não trata nenhuma operação específica de HTTP (redirecionamento, autenticação, suporte a proxy) nem executa operações de e/s (envio ou recebimento de bytes de fluxo do WebSocket).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[WinHTTP (serviços HTTP do Windows)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

