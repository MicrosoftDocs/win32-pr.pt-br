---
description: Em vez de enviar as chaves de sessão criptografadas para ambas as entidades de segurança, o KDC envia as cópias do cliente e do servidor da chave de sessão para o cliente.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Tíquetes de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762223311dd71f8bded5e021372d3a281f711eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811302"
---
# <a name="session-tickets"></a>Tíquetes de sessão

Em vez de enviar as chaves de sessão criptografadas para ambas as entidades de segurança, o [KDC](key-distribution-center.md) envia as cópias do cliente e do servidor da [*chave de sessão*](../secgloss/s-gly.md) para o cliente. A cópia da chave de sessão do cliente é criptografada com a [*chave mestra*](../secgloss/m-gly.md) do cliente e, portanto, não pode ser descriptografada por nenhuma outra entidade. A cópia da chave de sessão do servidor é inserida, juntamente com os dados de autorização sobre o cliente, em uma estrutura de dados chamada de tíquete. O tíquete é totalmente criptografado com a chave mestra do servidor e, portanto, não pode ser lido ou alterado pelo cliente ou por qualquer outra entidade que não tenha acesso à chave mestra do servidor. É responsabilidade do cliente armazenar o tíquete com segurança até entrar em contato com o servidor.

> [!Note]  
> O KDC fornece apenas um serviço de concessão de tíquetes. O cliente e o servidor são responsáveis por manter suas respectivas chaves mestras seguras.

 

Quando o cliente recebe a resposta do KDC, ele extrai o tíquete e sua própria cópia da chave de sessão, colocando-os de lado em um cache seguro. Para estabelecer uma sessão segura com o servidor, ele envia ao servidor uma mensagem que consiste no tíquete, ainda criptografado com a chave mestra do servidor e uma [mensagem de autenticador](authenticator-messages.md) criptografada com a chave de sessão. Juntos, a mensagem de tíquete e autenticador são as [*credenciais*](../secgloss/c-gly.md) do cliente para o servidor.

Quando o servidor recebe credenciais de um cliente, ele descriptografa o tíquete com sua [*chave mestra*](../secgloss/m-gly.md), extrai a chave de [*sessão*](../secgloss/s-gly.md)e usa a chave de sessão para descriptografar a mensagem do autenticador do cliente. Se tudo fizer check-out, o servidor saberá que as credenciais do cliente foram emitidas pelo KDC, uma autoridade confiável. Para a autenticação mútua, o servidor responde criptografando o carimbo de data/hora da mensagem do autenticador do cliente usando a chave de sessão. Essa mensagem criptografada é enviada ao cliente. Em seguida, o cliente descriptografa a mensagem. Se a mensagem retornada for a mesma do carimbo de data/hora na mensagem do autenticador original, o servidor será autenticado.

Como um benefício adicional, o servidor não precisa armazenar as chaves de sessão que ele usa com seus clientes. É responsabilidade de cada cliente gerenciar o tíquete para o servidor em seu cache de tíquetes e apresentar esse tíquete toda vez que ele acessar o servidor. Sempre que o servidor recebe um tíquete de um cliente, ele usa sua chave mestra para descriptografar o tíquete e extrair a chave de sessão. Quando o servidor não precisar mais da chave de sessão, a chave será excluída.

O cliente não precisa acessar o KDC cada vez que desejar acessar esse servidor específico. Tíquetes podem ser reutilizados. Como uma precaução contra a possibilidade de roubo de tíquete, os tíquetes têm um tempo de expiração, especificado pelo KDC na estrutura do tíquete. Por quanto tempo um tíquete é válido depende da política Kerberos para o realm. Normalmente, os tíquetes são bons por não mais do que oito horas, sobre o comprimento de uma [*sessão de logon*](../secgloss/l-gly.md)normal. Quando o usuário em uma estação de trabalho cliente faz logoff, o cache de tíquete do cliente é liberado e todas as permissões e as chaves de sessão do cliente são destruídas.

 

 
