---
description: Mostra como enviar uma mensagem criptografada.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Troca manual de chaves de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c9f7338b40ed1675b2186e478c8c124719b376889ce691d305e246016e0d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425586"
---
# <a name="manual-session-key-exchanges"></a>Troca manual de chaves de sessão

> [!Note]  
> O procedimento descrito nesta seção pressupõe que os usuários (ou clientes CryptoAPI) já possuem seu próprio conjunto de [*pares de chaves públicas/privadas*](../secgloss/p-gly.md) e também obteram [*as chaves públicas*](../secgloss/p-gly.md)de cada um deles.

 

A ilustração a seguir mostra como usar esse procedimento para enviar uma mensagem criptografada.

![enviando uma mensagem criptografada](images/capi04.png)

Essa abordagem é vulnerável a pelo menos uma forma comum de ataque. Um bisbilhoteiro pode adquirir cópias de uma ou mais mensagens criptografadas e as chaves criptografadas. Em seguida, em algum momento posterior, o bisbilhoteiro pode enviar uma dessas mensagens para o receptor e o receptor não terá como saber que a mensagem não foi proveniente diretamente do remetente original. Esse risco pode ser reduzido pelo carimbo de data/hora de todas as mensagens ou por meio de números de série.

A maneira mais fácil de enviar mensagens criptografadas para outro usuário é enviar a mensagem criptografada com uma chave de sessão aleatória junto com a chave de sessão criptografada com a chave [*pública de troca de chaves*](../secgloss/k-gly.md)do destinatário.

A seguir estão as etapas para enviar uma chave de sessão criptografada.

**Para enviar uma chave de sessão criptografada**

1.  Crie uma [*chave de sessão*](../secgloss/s-gly.md) aleatória usando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .
2.  Criptografe a mensagem usando a chave de sessão. Esse procedimento é discutido em [criptografia e](data-encryption-and-decryption.md)descriptografia de dados.
3.  Exporte a chave de sessão para um [*blob de chave*](../secgloss/k-gly.md) com a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , especificando que a chave seja criptografada com a chave pública de troca de chaves do usuário de destino.
4.  Envie a mensagem criptografada e o BLOB de chave criptografada para o usuário de destino.
5.  O usuário de destino importa o BLOB de chave para seu CSP usando a função [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) . Isso descriptografará automaticamente a chave de sessão, desde que a chave pública de troca de chaves do usuário de destino tenha sido especificada na etapa 3.
6.  O usuário de destino pode então descriptografar a mensagem usando a chave de sessão, seguindo o procedimento discutido em [criptografia e descriptografia de dados](data-encryption-and-decryption.md).

 

 
