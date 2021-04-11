---
description: Atributos de soquete do MultiPoint no Windows Sockets (Winsock).
ms.assetid: f6e779c6-dd9d-470e-aad9-715b69ad8c5f
title: Atributos de soquete do MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da67fd40c7c3bc7f1e9dbff22a3fef6cdaee4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164465"
---
# <a name="multipoint-socket-attributes"></a>Atributos de soquete do MultiPoint

Em alguns casos, os soquetes ingressados em uma sessão do MultiPoint podem ter algumas diferenças comportamentais de soquetes ponto a ponto. Por exemplo, um \_ soquete de folha d em um esquema de plano de dados com raiz só pode enviar informações para o \_ participante da raiz d. Isso cria uma necessidade de o cliente ser capaz de indicar o uso pretendido de um soquete coincidente com sua criação. Isso é feito por meio de quatro sinalizadores de atributo do MultiPoint que podem ser definidos por meio do parâmetro *dwFlags* em [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket):

-   \_O sinalizador \_ WSA \_ \_ raiz do MultiPoint C, para a criação de um soquete agindo como uma \_ raiz C e permitido somente se um plano de controle com raiz for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.
-   \_O sinalizador WSA do \_ MultiPoint \_ C \_ folha, para a criação de um soquete agindo como uma \_ folha C e permitido somente se o XP1 \_ oferecer suporte ao \_ MultiPoint for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.
-   \_O sinalizador WSA da \_ \_ raiz do MultiPoint D \_ , para a criação de um soquete agindo como uma \_ raiz D e permitido somente se um plano de dados com raiz for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.
-   \_O sinalizador WSA do \_ MultiPoint \_ D \_ folha, para a criação de um soquete agindo como uma \_ folha d e permitido somente se \_ o XP1 oferecer suporte ao \_ MultiPoint for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.

Ao criar um soquete do MultiPoint, exatamente um dos dois sinalizadores de plano de controle e um dos dois sinalizadores de plano de dados devem ser definidos no parâmetro *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Assim, as quatro possibilidades para criar soquetes do MultiPoint são: "c raiz \_ /d \_ raiz", "c \_ raiz/d \_ folha", "c \_ folha/d \_ raiz" ou "c \_ folha/d \_ folha".

 

 
