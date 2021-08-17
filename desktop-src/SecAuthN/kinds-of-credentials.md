---
description: Explica os dois tipos de credenciais com os quais a API de gerenciamento de credenciais funciona.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Tipos de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d0e067b3918496310f3244153864abbf7548e5367569f4f2fbd06de40f207c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140929"
---
# <a name="kinds-of-credentials"></a>Tipos de credenciais

A API de gerenciamento de credenciais funciona com dois tipos de credenciais:

-   [Credenciais de domínio](#domain-credentials)
-   [Credenciais genéricas](#generic-credentials)

## <a name="domain-credentials"></a>Credenciais do domínio

As credenciais de domínio são usadas pelo sistema operacional e autenticadas pela autoridade de segurança local (LSA). Normalmente, as credenciais de domínio são estabelecidas para um usuário quando um pacote de segurança registrado, como o protocolo Kerberos, autentica os dados de logon fornecidos pelo usuário. As credenciais de logon são armazenadas em cache pelo sistema operacional para que um logon único forneça ao usuário acesso a vários recursos diferentes. Por exemplo, as conexões de rede podem ocorrer de forma transparente e o acesso a objetos protegidos do sistema pode ser concedido com base nas credenciais de domínio em cache do usuário.

As funções de gerenciamento de credenciais fornecem um mecanismo para que os aplicativos solicitem a um usuário as credenciais de domínio depois que o usuário faz logon e que o sistema operacional autentique as informações fornecidas pelo usuário.

A parte secreta das credenciais de domínio, a senha, é protegida pelo sistema operacional. Somente o código em execução no processo com o LSA pode ler e gravar credenciais de domínio. Os aplicativos são limitados à gravação de credenciais de domínio.

o Windows dá suporte ao uso expandido de credenciais de cartão inteligente e certificado. Para ajudar a garantir a segurança, a API de gerenciamento de credenciais nunca armazena o PIN do cartão inteligente no computador.

## <a name="generic-credentials"></a>Credenciais genéricas

As credenciais genéricas são definidas e autenticadas por aplicativos que gerenciam a autorização e a segurança diretamente em vez de delegar essas tarefas para o sistema operacional. Por exemplo, um aplicativo pode exigir que os usuários insiram um nome de usuário e senha fornecidos pelo aplicativo ou produzam um [*certificado*](../secgloss/c-gly.md) para acessar um site.

Os aplicativos usam funções de gerenciamento de credenciais para solicitar aos usuários informações de credenciais, genéricas e definidas pelo aplicativo, como nome de usuário, certificado, cartão inteligente ou senha. As informações inseridas pelo usuário são retornadas ao aplicativo para autenticação.

O gerenciamento de credenciais fornece gerenciamento de cache personalizável e armazenamento de longo prazo para credenciais genéricas. As credenciais genéricas podem ser lidas e gravadas por processos de usuário.

 

 
