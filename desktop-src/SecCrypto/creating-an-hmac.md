---
description: Explica como criar um HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Criando um HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb600b00c0bfa3ac8af24cd297b1e2dd67933e2990216dafe84713ee5e831c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876657"
---
# <a name="creating-an-hmac"></a>Criando um HMAC

**Para calcular um HMAC**

1.  Obter um ponteiro para o CSP (Provedor de [*Serviços*](../secgloss/c-gly.md) criptográficos) da Microsoft chamando [**CryptAcquireContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
2.  Crie um identificador para um objeto [*de hash*](../secgloss/h-gly.md) [*HMAC*](../secgloss/h-gly.md)chamando [**CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) Passe CALG \_ HMAC no *parâmetro Algid.* Passe o alça de uma [*chave simétrica*](../secgloss/s-gly.md) no *parâmetro hKey.* Essa chave simétrica é a chave usada para calcular o HMAC.
3.  Especifique o tipo de hash a ser usado chamando [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) com o parâmetro *dwParam* definido como o valor HP \_ HMAC \_ INFO. O *parâmetro pbData* deve apontar para uma estrutura [**HMAC INFO \_ inicializada.**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info)
4.  Chame [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) para começar a calcular o HMAC dos dados. A primeira chamada para **CryptHashData** faz com que o valor da chave seja combinado usando o operador XOR com a cadeia de caracteres interna e os dados. O resultado da operação XOR é com o hashed e, em seguida, os dados de destino para o HMAC (apontados pelo parâmetro *pbData* passado na chamada para **CryptHashData**) são com hashed. Se necessário, chamadas subsequentes **para CryptHashData** podem ser feitas para concluir o hash dos dados de destino.
5.  Chame [**CryptGetHashParam com**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) o *parâmetro dwParam definido* como HP \_ HASHVAL. Essa chamada faz com que o hash interno seja concluído e a cadeia de caracteres externa seja combinada usando XOR com a chave. O resultado da operação XOR é com hash e, em seguida, o resultado do hash interno (concluído na etapa anterior) é com hash. O hash externo é então concluído e retornado no *parâmetro pbData* e no comprimento no *parâmetro dwDataLen.*

> [!Note]  
> Não use a mesma chave [*simétrica*](../secgloss/s-gly.md) ([*sessão*](../secgloss/s-gly.md)) para a criptografia de mensagens [*e Message Authentication Code*](../secgloss/m-gly.md) (MAC). Usar a mesma chave para ambos aumenta muito o risco de mensagens serem decodificadas por invasores.

 

 

 
