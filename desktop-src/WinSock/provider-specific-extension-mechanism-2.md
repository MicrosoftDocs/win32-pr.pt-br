---
description: A função WSAIoctl permite que os provedores de serviços ofereçam extensões de recurso específicas do provedor.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed627aefdfefda2bf4b395098f6680086fd37dd7a302d977d9bf238f77d89d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733566"
---
# <a name="provider-specific-extension-mechanism"></a>Provider-Specific de extensão

A [**função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permite que os provedores de serviços ofereçam extensões de recurso específicas do provedor. Esse mecanismo presume, é claro, que um aplicativo está ciente de uma extensão específica e compreende a semântica e a sintaxe envolvidas. Essas informações normalmente seriam fornecidas pelo fornecedor do provedor de serviços.

Para invocar uma função de extensão, o aplicativo deve primeiro solicitar um ponteiro para a função desejada. Isso é feito por meio [**da função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando o código de comando SIO \_ GET EXTENSION FUNCTION \_ \_ \_ POINTER. O buffer de entrada **para WSAIoctl** contém um identificador para a função de extensão desejada, enquanto o buffer de saída contém o ponteiro de função em si. O aplicativo pode invocar a função de extensão diretamente sem passar pelo Ws2 \_32.dll.

Os identificadores atribuídos às funções de extensão são GUIDs (identificadores globalmente exclusivos) alocados por fornecedores do provedor de serviços. Os fornecedores que criam funções de extensão são incentivados a publicar detalhes completos sobre a função, incluindo a sintaxe do protótipo de função. Isso possibilita que funções de extensão comuns e populares sejam oferecidas por mais de um fornecedor de provedor de serviços. Um aplicativo pode obter o ponteiro de função e usar a função sem precisar saber nada sobre o provedor de serviços específico que implementa a função.

No Windows Vista e posterior, novas extensões do sistema Winsock são exportadas diretamente da DLL winsock, portanto, a [**função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) não é necessária para carregar essas extensões. As novas funções de extensão disponíveis no Windows Vista e posterior incluem as funções [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) exportadas do *Ws2 \_32.dll*.

 

 
