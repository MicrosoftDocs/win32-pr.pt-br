---
title: Bluetooth e aceitar
description: O Bluetooth usa a função Accept para habilitar tentativas de conexão de entrada em um soquete.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- aceitar
- Bluetooth
- Bluetooth
- Bluetooth e aceitar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749133"
---
# <a name="bluetooth-and-accept"></a>Bluetooth e aceitar

O Bluetooth usa a função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar tentativas de conexão de entrada em um soquete. O \_ endereço de BTH do aplicativo cliente é obtido lendo a seção específica de transporte de Bluetooth da estrutura [**SOCKADDR**](/windows/desktop/WinSock/sockaddr-2) retornada. O uso da função **Accept** com Bluetooth tem o seguinte formato:

-   O parâmetro *addr* da função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) é um ponteiro opcional para um buffer que recebe o endereço da entidade de conexão, como conhecido pela camada de comunicação. Um ponteiro para uma estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) com o endereço de dispositivo Bluetooth remoto é retornado.
-   O parâmetro *addrlen* da função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) é um ponteiro opcional para um inteiro que contém o comprimento, em bytes, de addr. O inteiro deve ser maior ou igual ao valor de **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**aceitar**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 