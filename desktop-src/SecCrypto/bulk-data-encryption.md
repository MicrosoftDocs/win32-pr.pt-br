---
description: Uma chave de criptografia em massa é gerada pelo hash de uma das chaves MAC usando CryptHashSessionKey junto com o conteúdo da mensagem e outros dados. A mensagem é criptografada/descriptografada com uma das chaves de criptografia em massa da maneira usual.
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: Criptografia de dados em massa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecfb55c162e5aa576d8baa3d0ccbc45e9588c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753409"
---
# <a name="bulk-data-encryption"></a>Criptografia de dados em massa

Uma [*chave de criptografia em massa*](../secgloss/b-gly.md) é gerada pelo [*hash*](../secgloss/h-gly.md) de uma das chaves Mac usando [**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) junto com o conteúdo da mensagem e outros dados. A mensagem é criptografada/descriptografada com uma das chaves de criptografia em massa da maneira usual.

Ao usar uma [*codificação de bloco*](../secgloss/b-gly.md), o mecanismo de protocolo [*Schannel*](../secgloss/s-gly.md) faz todo o [*preenchimento*](../secgloss/p-gly.md)de *codificação de bloco* necessário. Quando [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) e [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) são chamados, o sinalizador final é sempre **false** e o comprimento dos dados é um múltiplo de comprimentos de bloco inteiros.

> [!Note]  
> O CSP nunca deve armazenar dados em buffer internamente. Depois que os dados são criptografados (ou descriptografados), o tamanho do [*texto não criptografado*](../secgloss/p-gly.md) deve sempre corresponder exatamente ao tamanho do [*texto cifrado*](../secgloss/c-gly.md).

 

 

 
