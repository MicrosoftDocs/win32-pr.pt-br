---
description: Em um protocolo simples usando a autenticação de chave secreta, um cliente apresenta uma mensagem de autenticador na forma de uma informação criptografada na chave de sessão.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Mensagens do autenticador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e76cf171d163ac2f1d0d4a7fcaab53a7fa0ace0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170028"
---
# <a name="authenticator-messages"></a>Mensagens do autenticador

Em um protocolo simples usando a autenticação de chave secreta, um cliente apresenta uma mensagem de autenticador na forma de uma informação criptografada na [*chave de sessão*](/windows/desktop/SecGloss/s-gly). As informações na mensagem do autenticador devem ser diferentes cada vez que o protocolo de autenticação é executado, ou uma mensagem de autenticador criptografado pode ser reutilizada por uma entidade não autorizada.

Ao receber a mensagem do autenticador, o servidor a descriptografa e pode contar com o conteúdo da mensagem descriptografada, independentemente de a descriptografia ter sido bem-sucedida. Se a mensagem descriptografada não for ininteligível, o servidor saberá que o cliente que está apresentando a mensagem do autenticador usou a chave correta para criptografar a mensagem. Somente duas entidades têm acesso à [*chave de sessão*](/windows/desktop/SecGloss/s-gly) e, se o servidor for um deles, o cliente que criptografou a mensagem de autenticador deverá ser o outro.

Para a autenticação mútua, um protocolo semelhante é executado. O servidor extrai parte das informações da mensagem de autenticador descriptografada e original, criptografa-a com a chave de sessão compartilhada e envia a mensagem criptografada para o cliente. O cliente descriptografa a mensagem e compara o resultado com o original. Se a mensagem descriptografada corresponder à parte correta da mensagem original, o cliente saberá que o servidor foi capaz de descriptografar a mensagem original com a chave de sessão de segredo compartilhado e foi capaz de criptografar novamente uma parte dessa mensagem com a mesma [*chave de sessão*](/windows/desktop/SecGloss/s-gly)de segredo compartilhado.

 

 
