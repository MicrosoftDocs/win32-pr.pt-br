---
description: Embora os provedores de serviço do Windows Sockets sejam incentivados a implementar soquetes como objetos de sistema de arquivos instaláveis (IFS), a arquitetura do Winsock também acomoda provedores de serviços cujas alças de soquete não são objetos IFS.
ms.assetid: ed5e10f4-fa17-4a07-9cac-43767915b8e9
title: Alocação de descritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095301798eb850fc4eb63e1939712379b5ead85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797956"
---
# <a name="descriptor-allocation"></a>Alocação de descritores

Embora os provedores de serviço do Windows Sockets sejam incentivados a implementar soquetes como objetos de sistema de arquivos instaláveis (IFS), a arquitetura do Winsock também acomoda provedores de serviços cujas alças de soquete não são objetos IFS. Provedores com identificadores IFS indicam isso por meio do XP1 \_ IFS \_ manipula o bit de atributo na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . (Observação: o XP1 \_ O \_ bits de atributo de identificadores IFS não foi incluído na versão 2.0.8 da especificação de API, mas já foi adicionado por meio do mecanismo de errata.) Os clientes do Winsock SPI podem aproveitar os provedores cujos descritores de soquete são identificadores de IFS usando esses descritores com instalações de e/s padrão do Windows, como [ReadFile](/windows/win32/api/fileapi/nf-fileapi-readfile) e [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile).

Sempre que um provedor de IFS cria um novo descritor de soquete, é obrigatório que o provedor chame [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) antes de fornecer o novo identificador a um cliente SPI do Windows Sockets. Essa função usa um identificador de provedor e um identificador IFS proposto do provedor como entrada e retorna um identificador modificado (possivelmente). O provedor de IFS deve fornecer apenas o identificador modificado para seu cliente e todas as solicitações do cliente referenciarão apenas esse identificador modificado. O identificador modificado é garantido como indistinguíveis do identificador proposto no que diz respeito ao sistema operacional. Portanto, na maioria dos casos, o provedor de serviços simplesmente optará por usar apenas o identificador modificado em todo o seu processamento interno. A finalidade dessa função de modificação é permitir que o32.dll de ws2 \_ simplifique muito o processo de identificação do provedor de serviços associado a um determinado soquete.

Provedores que não retornam identificadores de IFS devem obter um identificador válido do \_32.dll Ws2 por meio da chamada [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) . O provedor nonIFS deve oferecer apenas um identificador fornecido pelo Windows Sockets 2.DLL ao seu cliente e todas as solicitações do cliente referenciarão somente esses identificadores. Como uma conveniência para implementadores de provedores de serviços, um dos parâmetros de entrada fornecidos por um provedor em **WPUCreateSocketHandle** é um valor de contexto DWORD. O ws2 \_32.dll associa esse valor de contexto ao identificador de soquete alocado e permite que um provedor de serviços recupere o valor de contexto a qualquer momento por meio da chamada [**WPUQuerySocketHandleContext**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext) . Um uso típico para esse valor de contexto seria armazenar um ponteiro para uma estrutura de dados mantida pelo provedor de serviços usada para armazenar informações de estado do soquete.

 

 
