---
title: Log de Server-Side
description: O registro em log do lado do servidor está disponível em um grupo de URLs ou sessão de servidor.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8caf7475fe6d2b408f6e2a1f924bad73df64c315ef5e0acd1c7c317ce5eac6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829836"
---
# <a name="server-side-logging"></a>Log de Server-Side

O registro em log do lado do servidor está disponível em um grupo de URLs ou sessão de servidor. Quando o log está habilitado em uma sessão de servidor, ele funciona como uma forma centralizada de registro em log para todos os grupos de URLs na sessão do servidor. Quando o log está habilitado em um grupo de URLs, o log é executado somente em solicitações que são roteadas para o grupo de URLs. Os seguintes tipos de registro em log são suportados pela API do servidor HTTP:

-   [Log W3C](w3c-logging.md): disponível na sessão do servidor e no grupo de URLs.
-   [Log do NCSA](ncsa-logging.md): disponível no grupo de URLs.
-   [Log do IIS](iis-logging.md): disponível no grupo de URLs.
-   [Log binário centralizado](centralized-binary-logging.md): disponível na sessão do servidor.

Para aproveitar o recurso de log HTTP, o aplicativo habilita e configura um tipo de log na sessão de servidor ou no grupo de URLs. Para obter mais informações, consulte [Configurando e habilitando o log do servidor](configuring-and-enabling-server-side-logging.md)

 

 




