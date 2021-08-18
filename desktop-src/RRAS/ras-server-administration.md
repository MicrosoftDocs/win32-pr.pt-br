---
title: Administração do servidor RAS
description: Windows NT o servidor 4,0 fornece um conjunto de funções para administrar permissões e portas de usuário em servidores RAS Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administração do servidor, RAS
- Administração, servidor RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6760e8cc06e5c7b389d01f690497dc070974cada5e9a922ec5576e48b2a328fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789185"
---
# <a name="ras-server-administration"></a>Administração do servidor RAS

Windows NT o servidor 4,0 fornece um conjunto de funções para administrar permissões e portas de usuário em servidores RAS Windows NT/Windows 2000. Windows 95 não oferece suporte a essas funções. Usando essas funções, você pode desenvolver um aplicativo de administração de servidor RAS para executar as seguintes tarefas:

-   Enumerar os usuários que têm um conjunto especificado de permissões de RAS
-   Atribuir ou revogar permissões RAS para um usuário especificado
-   Enumerar as portas configuradas em um servidor RAS
-   Obter informações e estatísticas sobre uma porta especificada em um servidor RAS
-   Redefinir os contadores de estatísticas para uma porta especificada
-   Desconectar uma porta especificada

Você também pode instalar uma DLL de administração de servidor RAS para auditar conexões de usuário e atribuir endereços IP a usuários de discagem. A DLL exporta um conjunto de funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar.

 

 




