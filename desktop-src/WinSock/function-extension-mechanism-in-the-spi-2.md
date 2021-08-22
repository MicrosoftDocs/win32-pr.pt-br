---
description: Como a própria DLL do Winsock não é mais fornecida por cada fornecedor de pilha individual, não é possível que um fornecedor de pilha ofereça funcionalidade estendida adicionando pontos de entrada à DLL do Winsock.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Mecanismo de extensão de função no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2e5e32a4d79174893cfb2d9fa2ae0c0521a51ac80c40bcb6c45feab49693d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132419"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Mecanismo de extensão de função no SPI

Como a própria DLL do Winsock não é mais fornecida por cada fornecedor de pilha individual, não é possível que um fornecedor de pilha ofereça funcionalidade estendida adicionando pontos de entrada à DLL do Winsock. Para superar essa limitação, o Winsock aproveita a nova função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para acomodar os provedores de serviço que desejam oferecer extensões de funcionalidade específicas do provedor. Esse mecanismo pressupõe que um aplicativo esteja ciente de uma extensão específica e entenda a semântica e a sintaxe envolvidas. Essas informações normalmente seriam fornecidas pelo fornecedor do provedor de serviços.

Para invocar uma função de extensão, o aplicativo deve primeiro solicitar um ponteiro para a função desejada. Isso é feito por meio da função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando o \_ código de comando do ponteiro da função de extensão sio get \_ \_ \_ . O buffer de entrada para a função **WSAIoctl** contém um identificador para a função de extensão desejada e o buffer de saída conterá o próprio ponteiro de função. O aplicativo pode invocar a função de extensão diretamente sem passar pelo \_32.dll Ws2.

Os identificadores atribuídos às funções de extensão são identificadores globais exclusivos (GUIDs) alocados por fornecedores de provedor de serviços. Fornecedores que criam funções de extensão são instruídos a publicar detalhes completos sobre a função, incluindo a sintaxe do protótipo de função. Isso facilita a oferta de funções de extensão comuns e/ou populares por vários provedores de serviços. Um aplicativo pode obter o ponteiro de função e usar a função sem precisar saber nada sobre o provedor de serviços específico que implementa a função.

 

 



