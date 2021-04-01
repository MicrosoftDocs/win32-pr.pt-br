---
description: Muitas formas de autenticação se baseiam na ideia de que uma entidade pode provar sua identidade se puder provar que ela conhece uma chave, como uma senha, que só pode ser conhecida.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticação de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169828"
---
# <a name="key-authentication"></a>Autenticação de chave

Muitas formas de autenticação se baseiam na ideia de que uma entidade pode provar sua identidade se puder provar que ela conhece uma chave, como uma senha, que só pode ser conhecida.

As técnicas de autenticação que dependem de um segredo, como uma senha, precisam ter uma maneira de manter o segredo de se tornarem um conhecimento público. Um proprietário de senha não pode ir até uma porta e fornecer a senha. Alguém além do doorkeeper pode estar ouvindo; ou pode ser a porta errada. Para manter um segredo, deve haver uma maneira de provar que um usuário sabe a senha sem revelar a senha. Essa é a ideia por trás da autenticação de chave secreta, um método de verificação usado em todo o [*protocolo Kerberos*](../secgloss/k-gly.md).

Observe que o "segredo" na autenticação de chave secreta é que o processo de autenticação ocorre "em segredo"; ou seja, sem jamais revelar o conteúdo da chave.

Para que a autenticação de chave secreta funcione, as duas partes de uma transação devem compartilhar uma [*chave de sessão*](../secgloss/s-gly.md) criptográfica que também é secreta, conhecida apenas para elas e para nenhuma outra. A chave é [*simétrica*](../secgloss/s-gly.md); ou seja, é uma chave única usada para criptografia e descriptografia. Uma das partes no processo de autenticação comprova seu conhecimento da chave criptografando uma mensagem. A outra parte comprova seu conhecimento da chave descriptografando a mensagem.

 

 
