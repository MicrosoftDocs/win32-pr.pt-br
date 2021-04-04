---
title: API do servidor HTTP
description: A API do servidor HTTP permite que os aplicativos se comuniquem via HTTP sem usar o Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API do servidor HTTP
- API do servidor HTTP, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084535"
---
# <a name="http-server-api"></a>API do servidor HTTP

## <a name="purpose"></a>Finalidade

A API do servidor HTTP permite que os aplicativos se comuniquem via HTTP sem usar o Microsoft Internet Information Server (IIS). Os aplicativos podem se registrar para receber solicitações HTTP para URLs específicas, receber solicitações HTTP e enviar respostas HTTP. A API do servidor HTTP inclui suporte a SSL para que os aplicativos possam trocar dados por conexões HTTP seguras sem o IIS. Ele também foi projetado para funcionar com portas de conclusão de e/s.

## <a name="developer-audience"></a>Público de desenvolvedores

Essa API foi projetada para uso por programadores C/C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API do servidor HTTP tem suporte nos sistemas operacionais Windows Server 2003 e no Windows XP com Service Pack 2 (SP2). Lembre-se de que o Microsoft IIS 5 em execução no Windows XP com SP2 não é capaz de compartilhar a porta 80 com outros aplicativos HTTP em execução simultaneamente.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                           | Descrição                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Sobre a API do servidor HTTP](about-http-server-api.md)<br/>                   | Informações gerais sobre HTTP.<br/>                                                              |
| [Usando a API do servidor HTTP](using-http-server-api.md)<br/>                   | Guia de procedimentos para usar HTTP.<br/>                                                             |
| [Referência de API do servidor HTTP](http-server-api-reference.md)<br/>           | Documentação de funções específicas, estruturas e tipos de enumeração disponíveis em HTTP.<br/>    |
| [Aplicativo de exemplo do servidor HTTP](http-server-sample-application.md)<br/> | Um aplicativo de exemplo que mostra como usar a API do servidor HTTP para executar tarefas do lado do servidor.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[WinHTTP (serviços HTTP do Windows)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

