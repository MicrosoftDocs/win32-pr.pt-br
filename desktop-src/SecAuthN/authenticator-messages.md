---
description: Em um protocolo simples que usa a autenticação de chave secreta, um cliente apresenta uma mensagem de autenticador na forma de uma informação criptografada na chave de sessão.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Authenticator Mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc21cd87fbf1b725f276f138bcd0bd513658428ddd1296c4016542953bd8b86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035456"
---
# <a name="authenticator-messages"></a>Authenticator Mensagens

Em um protocolo simples que usa a autenticação de chave [*secreta,*](/windows/desktop/SecGloss/s-gly)um cliente apresenta uma mensagem de autenticador na forma de uma informação criptografada na chave de sessão . As informações na mensagem do autenticador devem ser diferentes sempre que o protocolo de autenticação for executado ou uma mensagem de autenticador criptografada pode ser reutilizado por uma entidade não autorizada.

Ao receber a mensagem do autenticador, o servidor a descriptografa e pode saber pelo conteúdo da mensagem descriptografada se a descriptografia foi bem-sucedida. Se a mensagem descriptografada não for falsa, o servidor saberá que o cliente que está apresentando a mensagem do autenticador usou a chave correta para criptografar a mensagem. Somente duas entidades têm [](/windows/desktop/SecGloss/s-gly) acesso à chave de sessão e, se o servidor for uma dessas entidades, o cliente que criptografou a mensagem do autenticador deverá ser o outro.

Para autenticação mútua, um protocolo semelhante é executado. O servidor extrai parte das informações da mensagem autenticador original descriptografada, criptografa-a com a chave de sessão compartilhada e envia a mensagem criptografada para o cliente. O cliente descriptografa a mensagem e compara o resultado com o original. Se a mensagem descriptografada corresponde à parte correta da mensagem original, o cliente sabe que o servidor foi capaz de descriptografar a mensagem original com a chave de sessão secreta compartilhada e conseguiu criptografar uma parte dessa mensagem com a mesma chave de sessão secreta [*compartilhada.*](/windows/desktop/SecGloss/s-gly)

 

 
