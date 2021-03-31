---
title: Suporte ao host de segurança RAS
description: O Windows NT 4,0 fornece uma maneira de uma DLL de segurança de RAS de terceiros para aprimorar os recursos de segurança RAS internos. O Windows 95 não oferece esse suporte.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Suporte a host, RAS
- Suporte ao host de segurança, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636315"
---
# <a name="ras-security-host-support"></a>Suporte ao host de segurança RAS

O Windows NT 4,0 fornece uma maneira de uma DLL de segurança de RAS de terceiros para aprimorar os recursos de segurança RAS internos. O Windows 95 não oferece esse suporte.

Um servidor RAS do Windows NT/Windows 2000 fornece mecanismos de segurança para validar o acesso à rede de usuários remotos. Quando um servidor RAS recebe uma chamada, ele valida as credenciais do usuário em relação ao banco de dados de conta local ou de domínio. O RAS também dá suporte à segurança de retorno de chamada, na qual o servidor RAS desliga e, em seguida, chama o usuário remoto para estabelecer a conexão. Para redes em que esse nível de segurança não é suficiente, você pode instalar uma DLL de segurança de RAS de terceiros. A DLL de segurança pode autenticar um usuário remoto, lendo informações de segurança de um banco de dados diferente do banco de dados da conta de usuário padrão.

Quando o servidor RAS recebe uma chamada, ele invoca a DLL de segurança para autenticar o usuário remoto. O suporte ao host de segurança RAS fornece um mecanismo para que a DLL de segurança se comunique com o usuário remoto por meio de uma janela de terminal no computador remoto. Em um cenário típico, a DLL de segurança solicita o nome de logon do usuário remoto. Em seguida, a DLL usa seu banco de dados de segurança privada para formular um desafio para enviar ao terminal remoto. Por exemplo, o desafio pode ser um código que o usuário deve fornecer como entrada para um leitor de Cardkey. O leitor do Cardkey, em seguida, exibe uma resposta que o usuário remoto digita na janela do terminal. Em seguida, a DLL de segurança valida a resposta em relação às informações do usuário no banco de dados de segurança privada.

Se a DLL de segurança autenticar o usuário remoto, o servidor RAS executará sua própria autenticação. Isso garante que a segurança RAS sempre autentique um usuário remoto, mesmo que uma DLL de segurança esteja instalada que conceda acesso a todos os usuários.

> [!Note]  
> O Windows NT/Windows 2000 atualmente fornece suporte ao host de segurança RAS somente para conexões de modem assíncronas; outros tipos de conexões, como Ethernet (que não é uma conexão de modem), VPN (que também não é uma conexão de modem) ou ISDN (que é síncrono), não têm suporte.

 

 

 




