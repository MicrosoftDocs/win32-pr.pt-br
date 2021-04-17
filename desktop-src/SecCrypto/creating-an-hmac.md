---
description: Explica como criar um HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Criando um HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364314081bd1d84d6d9bfff889c234470cc6775c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753719"
---
# <a name="creating-an-hmac"></a>Criando um HMAC

**Para calcular um HMAC**

1.  Obtenha um ponteiro para o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) da Microsoft chamando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
2.  Crie um identificador para um objeto [*HMAC*](../secgloss/h-gly.md)[*hash*](../secgloss/h-gly.md) chamando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Passe CALG \_ HMAC no parâmetro *algid* . Passe o identificador de uma [*chave simétrica*](../secgloss/s-gly.md) no parâmetro *HKEY* . Essa chave simétrica é a chave usada para calcular o HMAC.
3.  Especifique o tipo de hash a ser usado chamando [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) com o parâmetro *dwParam* definido como o valor HP \_ HMAC \_ info. O parâmetro *pbData* deve apontar para uma estrutura [**de \_ informações HMAC**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) inicializada.
4.  Chame [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) para começar a computar o HMAC dos dados. A primeira chamada para **CryptHashData** faz com que o valor da chave seja combinado usando o operador XOR com a cadeia de caracteres interna e os dados. O resultado da operação XOR é de hash e, em seguida, os dados de destino para o HMAC (apontado pelo parâmetro *pbData* passado na chamada para **CryptHashData**) são com hash. Se necessário, as chamadas subsequentes para **CryptHashData** podem então ser feitas para concluir o hash dos dados de destino.
5.  Chame [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) com o parâmetro *DWPARAM* definido como HP \_ HASHVAL. Essa chamada faz com que o hash interno seja concluído e a cadeia de caracteres externa seja combinada usando XOR com a chave. O resultado da operação XOR é de hash e, em seguida, o resultado do hash interno (concluído na etapa anterior) é de hash. Em seguida, o hash externo é concluído e retornado no parâmetro *pbData* e o comprimento no parâmetro *dwDataLen* .

> [!Note]  
> Não use a mesma chave [*simétrica*](../secgloss/s-gly.md) ([*sessão*](../secgloss/s-gly.md)) para a geração de criptografia de mensagem e de [*Message Authentication Code*](../secgloss/m-gly.md) (Mac). Usar a mesma chave para aumentar muito o risco de mensagens sendo decodificadas por invasores.

 

 

 
