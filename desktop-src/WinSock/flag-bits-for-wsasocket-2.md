---
description: Em alguns casos, os soquetes ingressados em uma sessão do MultiPoint podem ter algumas diferenças no comportamento de soquetes ponto a ponto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Marcar bits para WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807887"
---
# <a name="flag-bits-for-wsasocket"></a>Marcar bits para WSASocket

Em alguns casos, os soquetes ingressados em uma sessão do MultiPoint podem ter algumas diferenças no comportamento de soquetes ponto a ponto. Por exemplo, um \_ soquete de folha d em um esquema de plano de dados com raiz só pode enviar informações para o \_ participante da raiz d. Isso cria uma necessidade de o aplicativo ser capaz de indicar o uso pretendido de um soquete coincidente com sua criação. Isso é feito por meio de bits de quatro sinalizadores que podem ser definidos no parâmetro *dwFlags* para [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):

-   \_O sinalizador \_ WSA \_ \_ raiz do MultiPoint C, para a criação de um soquete agindo como uma \_ raiz C e permitido somente se um plano de controle com raiz for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.
-   \_O sinalizador WSA do \_ MultiPoint \_ C \_ folha, para a criação de um soquete agindo como uma \_ folha C e permitido somente se o XP1 \_ oferecer suporte ao \_ MultiPoint for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.
-   \_O sinalizador WSA da \_ \_ raiz do MultiPoint D \_ , para a criação de um soquete agindo como uma \_ raiz D e permitido somente se um plano de dados com raiz for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.
-   \_O sinalizador WSA do \_ MultiPoint \_ D \_ folha, para a criação de um soquete agindo como uma \_ folha d e permitido somente se \_ o XP1 oferecer suporte ao \_ MultiPoint for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.

Observe que, ao criar um soquete do MultiPoint, exatamente um dos dois sinalizadores de plano de controle e um dos dois sinalizadores de plano de dados devem ser definidos no parâmetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Portanto, as quatro possibilidades para criar soquetes do MultiPoint são:

-   " \_ raiz c raiz/d \_ "
-   "c \_ raiz/d \_ folha"
-   "c \_ folha/d \_ raiz"
-   "c \_ folha/d \_ folha"

 

 
