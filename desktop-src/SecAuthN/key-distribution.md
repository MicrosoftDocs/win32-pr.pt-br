---
description: A técnica de autenticação de chave secreta não explica como o cliente e o servidor obterão a chave de sessão secreta a ser usada em sessões entre si.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Distribuição de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd39f9cd5e219ac1e6339c0a6c3e7b9a19dc2680c21e948bdb979af791719a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013326"
---
# <a name="key-distribution"></a>Distribuição de chaves

A técnica de autenticação de chave secreta não explica como o cliente e o servidor obterão a chave de sessão [*secreta*](../secgloss/s-gly.md) a ser usada em sessões entre si. Se elas são pessoas, elas podem se encontrar em segredo e concordar com a chave. Mas se o cliente for um programa em execução em uma estação de trabalho e o servidor for um serviço em execução em um servidor de rede, esse método não funcionará.

Um cliente deseja se comunicar com muitos servidores e precisará de chaves diferentes para cada um deles. Um servidor se comunica com muitos clientes e precisa de chaves diferentes para cada um deles também. Se cada cliente precisar de uma chave diferente para cada servidor e cada servidor precisar de uma chave diferente para cada cliente, a distribuição de chaves se tornará um problema. Além disso, a necessidade de armazenar e proteger muitas chaves em muitos computadores cria um enorme risco de segurança.

O nome do protocolo [*Kerberos sugere*](../secgloss/k-gly.md) sua solução para o problema de distribuição de chaves. Kerberos (ou Cerberus) era uma figura na filosofia clássica do grego – um cachorro de três cabeça, que mantém invasores vivos de entrar no Ataque. Assim como a proteção imática, o protocolo Kerberos tem três caras: um cliente, um servidor e um terceiro confiável para mediar entre eles. O intermediário confiável nesse protocolo é o KDC (centro de distribuição de chaves).

O KDC é um serviço em execução em um servidor fisicamente seguro. Ele mantém um banco de dados com informações de conta para todas [*as entidades de segurança*](../secgloss/s-gly.md) em seu realm. Um realm é o equivalente kerberos de um domínio em Windows.

Juntamente com outras informações sobre cada entidade de segurança, o KDC armazena uma chave criptográfica conhecida apenas pela entidade de segurança e pelo KDC. Essa é a [*chave mestra*](../secgloss/m-gly.md) usada em trocas entre cada entidade de segurança e o KDC. Na maioria das implementações do protocolo Kerberos, essa chave mestra é derivada usando uma função [*de hash*](../secgloss/h-gly.md) da senha de uma entidade de segurança.

Quando um cliente deseja criar uma conexão segura com um servidor, o cliente começa enviando uma solicitação para o KDC, não para o servidor que ele deseja alcançar. O KDC cria e envia ao cliente uma chave de sessão [*exclusiva*](../secgloss/s-gly.md) para o cliente e um servidor usar para autenticar uns aos outros. O KDC tem acesso à chave mestra do cliente e à chave mestra do servidor. O KDC criptografa a cópia do servidor da chave de sessão usando a chave mestra do servidor e a cópia do cliente usando a chave mestra do cliente.

O KDC poderia cumprir sua função como intermediário confiável enviando a chave de sessão diretamente para cada uma das entidades de segurança envolvidas, mas, na prática, esse procedimento não funcionará por vários motivos. Em vez disso, o KDC envia as duas chaves de sessão criptografadas para o cliente. A chave de sessão para o servidor está incluída em um [tíquete de sessão](session-tickets.md).

 

 
