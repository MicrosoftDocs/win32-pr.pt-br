---
description: O provedor criptográfico RSA avançado da Microsoft e AES oferece suporte aos mesmos recursos que o provedor Microsoft Base Cryptographic, chamado provedor base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Provedor criptográfico do Microsoft AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb4c774eb2cb9d01bcb3a12f5550537abe44b364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755042"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Provedor criptográfico do Microsoft AES

O provedor criptográfico RSA avançado da Microsoft e AES oferece suporte aos mesmos recursos que o provedor Microsoft Base Cryptographic, chamado provedor base. O provedor AES dá suporte à segurança mais forte por meio de chaves mais longas e algoritmos adicionais. Ele pode ser usado com todas as versões do CryptoAPI.

**Windows XP:** O provedor criptográfico do Microsoft AES foi nomeado Microsoft Enhanced RSA e AES (provedor criptográfico).

Para manter a compatibilidade com versões anteriores do provedor, o nome do provedor, conforme definido no arquivo de cabeçalho Wincrypt. h, retém a designação da versão 1,0, embora as versões mais recentes desse provedor tenham sido enviadas. Para determinar a versão do provedor em uso, chame [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o parâmetro *DWPARAM* definido como PP \_ version. A versão 2,0 estará em uso se 0x0200 for retornado.

|                |                             |
|----------------|-----------------------------|
| Tipo de provedor: | **PROV \_ RSA \_ AES**          |
| Nome do provedor: | **\_ENH \_ RSA \_ AES \_ da Microsoft** |



 

A tabela a seguir realça as diferenças entre o provedor base, o provedor forte e o provedor AES. Os [*comprimentos de chave*](../secgloss/k-gly.md) mostrados são os comprimentos de chave padrão.



| Algoritmo                                                                                | Comprimento da chave do provedor base | Comprimento da chave do provedor forte | Comprimento da chave do provedor AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de assinatura de chave pública RSA                                                       | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de troca de chave pública RSA                                                        | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de criptografia de bloco RC2                                                           | 40 bits                  | 128 bits                   | o comprimento de Salt de 128 bits pode ser definido.<br/> |
| Algoritmo de criptografia de fluxo RC4                                                          | 40 bits                  | 128 bits                   | o comprimento de Salt de 128 bits pode ser definido.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Des triplo*](../secgloss/t-gly.md) (2 teclas) | Sem suporte            | 112 bits                   | 112 bits                                    |
| DES triplo (3 teclas)                                                                       | Sem suporte            | 168 bits                   | 168 bits                                    |



 

Para obter uma lista completa dos algoritmos com suporte, consulte [algoritmos do provedor AES](aes-provider-algorithms.md).

O provedor forte, o provedor avançado e o provedor AES são compatíveis com versões anteriores com o provedor base, exceto que os provedores podem gerar apenas chaves RC2 ou RC4 de comprimento de chave padrão. O comprimento padrão para o provedor de base é de 40 bits. O comprimento padrão para o provedor AES é de 128 bits. Portanto, o provedor AES não pode criar chaves com comprimentos de chave compatíveis com o provedor base. No entanto, o provedor AES pode importar chaves RC2 e RC4 de até 128 bits. Portanto, o provedor AES pode importar e usar chaves de 40 bits geradas usando o provedor base.

 

 
