---
title: Conectando o cliente e o servidor
description: Para se comunicar, os programas de cliente e servidor devem estabelecer uma sessão de comunicação na rede ou nas redes que os conectam.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Chamada de procedimento remoto RPC, tarefas, cliente de conexão e servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f477802ffb4b72f33ce951bf811b1cb9b770a8272f646507dfaa450934569f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931223"
---
# <a name="connecting-the-client-and-the-server"></a>Conectando o cliente e o servidor

Para se comunicar, os programas de cliente e servidor devem estabelecer uma sessão de comunicação na rede ou nas redes que os conectam. Depois que eles estabelecem a conexão, o cliente pode chamar procedimentos remotos no programa do servidor como se eles fossem locais para o programa cliente.

Esta seção fornece uma visão geral conceitual de como estabelecer uma conexão entre clientes e servidores para chamadas de procedimento remoto. Ele não fornece uma discussão aprofundada sobre este tópico. Todos os conceitos nesta seção são apresentados em detalhes em capítulos posteriores e na seção de referência da função RPC.

A discussão apresentada nesta seção está dividida nos seguintes tópicos:

-   [Terminologia de ligação de RPC essencial](essential-rpc-binding-terminology.md)
-   [Como o servidor se prepara para uma conexão](how-the-server-prepares-for-a-connection.md)
-   [Como o cliente estabelece uma conexão](how-the-client-establishes-a-connection.md)

Observe que a discussão pressupõe identificadores de ligação explícitos. No entanto, se seu aplicativo usar outros tipos de identificadores de associação, talvez seja necessário modificar as etapas apresentadas nesta seção. Para obter mais informações, consulte [Binding e Handles](binding-and-handles.md).

 

 




