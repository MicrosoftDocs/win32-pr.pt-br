---
description: Muitas formas de autenticação se baseiam na ideia de que uma entidade pode provar sua identidade se puder provar que conhece uma chave, como uma senha, que somente ela pode saber.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticação de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9273bc3fc57bca5157431ce78495f2b5c4b97595ed8513ba76fa068ef76fe0b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787258"
---
# <a name="key-authentication"></a>Autenticação de chave

Muitas formas de autenticação se baseiam na ideia de que uma entidade pode provar sua identidade se puder provar que conhece uma chave, como uma senha, que somente ela pode saber.

As técnicas de autenticação que dependem de um segredo, como uma senha, precisam ter uma maneira de impedir que o segredo se torne conhecimento público. Um proprietário de senha não pode ir até uma porta e dar a senha. Alguém além do doorkeeper pode estar escutando; ou pode ser a porta errada. Para manter um segredo, deve haver uma maneira de provar que um usuário sabe a senha sem revelar a senha. Essa é a ideia por trás da autenticação de chave secreta, um método de verificação usado em todo o [*protocolo Kerberos*](../secgloss/k-gly.md).

Observe que o "segredo" na autenticação de chave secreta é que o processo de autenticação ocorre "em segredo", ou seja, sem realmente revelar o conteúdo da chave.

Para que a autenticação de chave secreta funcione, [](../secgloss/s-gly.md) as duas partes de uma transação devem compartilhar uma chave de sessão criptográfica que também é secreta, conhecida apenas por elas e por nenhuma outra. A chave é [*simétrica;*](../secgloss/s-gly.md) ou seja, é uma única chave usada para criptografia e descriptografia. Uma parte no processo de autenticação prova seu conhecimento da chave criptografando uma mensagem. A outra parte prova seu conhecimento da chave descriptografando a mensagem.

 

 
