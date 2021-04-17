---
title: Sobre a administração do serviço de acesso remoto
description: O Windows 2000 e sistemas operacionais posteriores fornecem um conjunto de funções para administrar permissões e portas de usuário em servidores RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- Serviço de roteamento e acesso remoto RRAS, administração de RAS
- Serviço de roteamento e acesso remoto RRAS, administração de RAS, descrito
- RRAS de administração RAS
- Administração de RAS RRAS, descrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759604"
---
# <a name="about-remote-access-service-administration"></a>Sobre a administração do serviço de acesso remoto

O Windows 2000 e sistemas operacionais posteriores fornecem um conjunto de funções para administrar permissões e portas de usuário em servidores RAS. Usando essas funções, você pode desenvolver um aplicativo de administração de servidor RAS para executar as seguintes tarefas:

-   Enumerar os usuários que têm um conjunto especificado de permissões de RAS
-   Atribuir ou revogar permissões RAS para um usuário especificado
-   Enumerar as portas configuradas em um servidor RAS
-   Obter informações e estatísticas sobre uma porta especificada em um servidor RAS
-   Redefinir os contadores de estatísticas para uma porta especificada
-   Desconectar uma porta especificada

Você também pode instalar uma DLL de administração do servidor RAS para auditar conexões de usuário e atribuir endereços IP a usuários de discagem. A DLL exporta um conjunto de funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar.

Esta documentação descreve os seguintes tópicos:

-   [Comparação de funções: Windows 2000 x RRAS redistribuível](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [Administração de usuário RAS](ras-user-administration.md)
-   [Administração de porta e servidor RAS](ras-server-and-port-administration.md)
-   [DLL de administração de RAS](ras-administration-dll.md)
-   [Configuração do registro da DLL de administração do RAS](ras-administration-dll-registry-setup.md)

 

 




