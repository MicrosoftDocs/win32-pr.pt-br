---
description: A técnica de autenticação de chave secreta não explica como o cliente e o servidor obtêm a chave de sessão secreta para usar em sessões entre si.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Distribuição de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a2968e8b7b978bc7b325d65b4a2acf08e1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662325"
---
# <a name="key-distribution"></a>Distribuição de chaves

A técnica de autenticação de chave secreta não explica como o cliente e o servidor obtêm a [*chave de sessão*](../secgloss/s-gly.md) secreta para usar em sessões entre si. Se forem pessoas, eles poderiam se reunir em segredo e concordar com a chave. Mas se o cliente for um programa em execução em uma estação de trabalho e o servidor for um serviço em execução em um servidor de rede, esse método não funcionará.

Um cliente vai querer se comunicar com vários servidores e precisará de chaves diferentes para cada um deles. Um servidor se comunica com muitos clientes e precisa de chaves diferentes para cada um deles também. Se cada cliente precisar de uma chave diferente para cada servidor, e cada servidor precisar de uma chave diferente para cada cliente, a distribuição de chave se tornará um problema. Além disso, a necessidade de armazenar e proteger muitas chaves em muitos computadores cria um enorme risco de segurança.

O nome do [*protocolo Kerberos*](../secgloss/k-gly.md) sugere sua solução para o problema de distribuição de chave. O Kerberos (ou O Cerberus) foi uma figura em grego da Grécia Mythology — uma selvagens, um cachorro de três pontas que mantinha intrusos de entrar no Underworld. Assim como o mítico Guard, o protocolo Kerberos tem três cabeçotes: um cliente, um servidor e um terceiro confiável para mediar entre eles. O intermediário confiável nesse protocolo é o centro de distribuição de chaves (KDC).

O KDC é um serviço em execução em um servidor fisicamente seguro. Ele mantém um banco de dados com informações de conta para todas as [*entidades de segurança*](../secgloss/s-gly.md) em seu Realm. Um realm é o equivalente Kerberos de um domínio no Windows.

Juntamente com outras informações sobre cada entidade de segurança, o KDC armazena uma chave criptográfica conhecida somente para o principal e o KDC. Essa é a [*chave mestra*](../secgloss/m-gly.md) usada em trocas entre cada entidade de segurança e o KDC. Na maioria das implementações do protocolo Kerberos, essa chave mestra é derivada usando uma função de [*hash*](../secgloss/h-gly.md) da senha de uma entidade de segurança.

Quando um cliente deseja criar uma conexão segura com um servidor, o cliente começa enviando uma solicitação para o KDC, não para o servidor que deseja alcançar. O KDC cria e envia ao cliente uma chave de [*sessão*](../secgloss/s-gly.md) exclusiva para o cliente e um servidor a ser usado para autenticar um ao outro. O KDC tem acesso à chave mestra do cliente e à chave mestra do servidor. O KDC criptografa a cópia da chave de sessão do servidor usando a chave mestra do servidor e a cópia do cliente usando a chave mestra do cliente.

O KDC pode atender à sua função como intermediário confiável enviando a chave de sessão diretamente para cada uma das entidades de segurança envolvidas, mas, na prática, esse procedimento não funcionará, por vários motivos. Em vez disso, o KDC envia ambas as chaves de sessão criptografadas para o cliente. A chave de sessão do servidor está incluída em um [tíquete de sessão](session-tickets.md).

 

 
