---
description: XP1 \_ oferece suporte \_ a parâmetros de atributo MultiPoint, XP1 \_ MultiPoint \_ Control \_ e XP1 \_ MultiPoint \_ Data \_ plano na estrutura de informações do Winsock WSAPROTOCOL \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Atributos na estrutura WSAPROTOCOL_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb502c0f29f09604f80e5437774f2b481cef238aaf34f566e78886127dae1027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898546"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Atributos na estrutura de informações de WSAPROTOCOL \_

Para dar suporte à taxonomia descrita acima, três parâmetros de atributo na estrutura [**de \_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) são usados para distinguir os esquemas usados nos planos de controle e de dados, respectivamente:

-   XP1 \_ suporte \_ a MultiPoint com um valor de 1 indica que essa entrada de protocolo dá suporte a comunicações do MultiPoint e que os dois parâmetros a seguir são significativos.
-   \_ \_ \_ O plano de controle do MultiPoint XP1 indica se o plano de controle tem raiz (valor = 1) ou não raiz (valor = 0).
-   \_ \_ \_ O plano de dados do MultiPoint XP1 indica se o plano de dados tem raiz (valor = 1) ou não raiz (valor = 0).

Observe que duas entradas de [**\_ informações WSAPROTOCOLs**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarão presentes se um protocolo multiponto tiver suporte para os planos de dados com e sem raiz, uma entrada para cada um.

O aplicativo pode usar o [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para descobrir se há suporte para comunicações do MultiPoint para um determinado protocolo e, em caso afirmativo, como há suporte em relação aos planos de controle e de dados, respectivamente.

 

 
