---
description: A função WSAIoctl permite que os provedores de serviços ofereçam extensões de recurso específicas do provedor.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Mecanismo de extensão de Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58a8bba3c83e7dbf973ff8fe5b7d91c1065cfc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090361"
---
# <a name="provider-specific-extension-mechanism"></a>Mecanismo de extensão de Provider-Specific

A função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permite que os provedores de serviços ofereçam extensões de recurso específicas do provedor. Esse mecanismo pressupõe, é claro, que um aplicativo esteja ciente de uma extensão específica e entenda a semântica e a sintaxe envolvidas. Essas informações normalmente seriam fornecidas pelo fornecedor do provedor de serviços.

Para invocar uma função de extensão, o aplicativo deve primeiro solicitar um ponteiro para a função desejada. Isso é feito por meio da função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando o \_ código de comando do ponteiro da função de extensão sio get \_ \_ \_ . O buffer de entrada para **WSAIoctl** contém um identificador para a função de extensão desejada, enquanto o buffer de saída contém o próprio ponteiro de função. O aplicativo pode invocar a função de extensão diretamente sem passar pelo \_32.dll Ws2.

Os identificadores atribuídos às funções de extensão são identificadores globais exclusivos (GUIDs) alocados por fornecedores de provedor de serviços. Fornecedores que criam funções de extensão são instruídos a publicar detalhes completos sobre a função, incluindo a sintaxe do protótipo de função. Isso possibilita que as funções de extensão comuns e populares sejam oferecidas por mais de um fornecedor de provedor de serviços. Um aplicativo pode obter o ponteiro de função e usar a função sem precisar saber nada sobre o provedor de serviços específico que implementa a função.

No Windows Vista e posterior, novas extensões de sistema Winsock são exportadas diretamente da DLL do Winsock, portanto, a função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) não é necessária para carregar essas extensões. As novas funções de extensão disponíveis no Windows Vista e versões posteriores incluem as funções [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) exportadas do *Ws2 \_32.dll*.

 

 
