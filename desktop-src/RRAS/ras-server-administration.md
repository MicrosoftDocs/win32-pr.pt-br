---
title: Administração do servidor RAS
description: O Windows NT Server 4,0 fornece um conjunto de funções para administrar permissões e portas de usuário em servidores Windows NT/Windows 2000 RAS.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administração do servidor, RAS
- Administração, servidor RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160263"
---
# <a name="ras-server-administration"></a>Administração do servidor RAS

O Windows NT Server 4,0 fornece um conjunto de funções para administrar permissões e portas de usuário em servidores Windows NT/Windows 2000 RAS. O Windows 95 não oferece suporte a essas funções. Usando essas funções, você pode desenvolver um aplicativo de administração de servidor RAS para executar as seguintes tarefas:

-   Enumerar os usuários que têm um conjunto especificado de permissões de RAS
-   Atribuir ou revogar permissões RAS para um usuário especificado
-   Enumerar as portas configuradas em um servidor RAS
-   Obter informações e estatísticas sobre uma porta especificada em um servidor RAS
-   Redefinir os contadores de estatísticas para uma porta especificada
-   Desconectar uma porta especificada

Você também pode instalar uma DLL de administração de servidor RAS para auditar conexões de usuário e atribuir endereços IP a usuários de discagem. A DLL exporta um conjunto de funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar.

 

 




