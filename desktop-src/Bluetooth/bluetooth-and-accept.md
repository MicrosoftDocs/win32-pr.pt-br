---
title: Bluetooth e aceitar
description: Bluetooth usa a função accept para habilitar tentativas de conexão de entrada em um soquete.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accept
- Bluetooth
- Bluetooth
- Bluetooth e aceitar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5f12a7fd9fee508354dfcd9421f830e814eed09bb207cc6024b50705cc3566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004606"
---
# <a name="bluetooth-and-accept"></a>Bluetooth e aceitar

Bluetooth usa a função [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar tentativas de conexão de entrada em um soquete. o \_ endereço de BTH do aplicativo cliente é obtido lendo a seção Bluetooth de transporte específica da estrutura [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) retornada. o uso da função **accept** com Bluetooth tem o seguinte formato:

-   O parâmetro *addr* da função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) é um ponteiro opcional para um buffer que recebe o endereço da entidade de conexão, como conhecido pela camada de comunicação. um ponteiro para uma estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) com o endereço de dispositivo Bluetooth remoto é retornado.
-   O parâmetro *addrlen* da função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) é um ponteiro opcional para um inteiro que contém o comprimento, em bytes, de addr. O inteiro deve ser maior ou igual ao valor de **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**aceitar**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 