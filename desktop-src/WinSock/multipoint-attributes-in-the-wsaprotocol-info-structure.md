---
title: Atributos do MultiPoint no WSAPROTOCOL_INFO
description: Os atributos do MultiPoint na \_ estrutura de informações do WSAPROTOCOL incluem XP1 \_ \_ MULTIPONTO MultiPoint, XP1 \_ MultiPoint \_ Control \_ plano e XP1 \_ MultiPoint \_ Data \_ Plane.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1275b6da00258be10b071bc9b2399abaf5dd608583f3d81a0fdb16af493824ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741100"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>Atributos do MultiPoint no WSAPROTOCOL_INFO

Três parâmetros de atributo são definidos na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir os diferentes esquemas usados nos planos de controle e de dados, respectivamente:

-   XP1 \_ suporte \_ a MultiPoint com um valor de 1 indica que essa entrada de protocolo dá suporte a comunicações do MultiPoint e que os dois parâmetros a seguir são significativos.
-   \_ \_ \_ O plano de controle do MultiPoint XP1 indica se o plano de controle tem raiz (valor = 1) ou não raiz (valor = 0).
-   \_ \_ \_ O plano de dados do MultiPoint XP1 indica se o plano de dados tem raiz (valor = 1) ou não raiz (valor = 0).

Duas entradas de [**\_ informações WSAPROTOCOLs**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarão presentes se um protocolo multiponto suportasse os planos de dados com e sem raiz, uma entrada para cada um.

 

 
