---
description: O Provedor de Criptografia AES e RSA aprimorado da Microsoft dá suporte aos mesmos recursos que o Provedor criptográfico base da Microsoft, chamado de Provedor Base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Provedor criptográfico do Microsoft AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2449c53cb828a94c8dd596133c3a8c21c9b0388
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581864"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Provedor criptográfico do Microsoft AES

O Provedor de Criptografia AES e RSA aprimorado da Microsoft dá suporte aos mesmos recursos que o Provedor criptográfico base da Microsoft, chamado de Provedor Base. O Provedor AES dá suporte à segurança mais forte por meio de chaves mais longas e algoritmos adicionais. Ele pode ser usado com todas as versões do CryptoAPI.

**Windows XP:** O Provedor criptográfico do Microsoft AES foi nomeado Microsoft Enhanced RSA e AES Cryptographic Provider (Protótipo).

Para manter a compatibilidade com versões anteriores do provedor, o nome do provedor, conforme definido no arquivo de título Wincrypt.h, retém a designação da versão 1.0, embora as versões mais recentes desse provedor tenham sido enviadas. Para determinar a versão do provedor em uso, chame [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o *parâmetro dwParam definido* como PP \_ VERSION. A versão 2.0 está em uso se 0x0200 é retornado.

|                   | Valor                    |
|-------------------|--------------------------|
| **Tipo de provedor** | PROV \_ RSA \_ AES           |
| **Nome do provedor** | MS \_ ENH \_ RSA \_ AES \_ PROV  |



 

A tabela a seguir destaca as diferenças entre o Provedor Base, o Provedor Forte e o Provedor AES. Os [*comprimentos de chave mostrados*](../secgloss/k-gly.md) são os comprimentos de chave padrão.



| Algoritmo                                                                                | Comprimento da chave do provedor base | Comprimento da chave do Provedor Forte | Comprimento da chave do Provedor AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de assinatura de chave pública RSA                                                       | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de troca de chaves públicas RSA                                                        | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de criptografia de bloco RC2                                                           | 40 bits                  | 128 bits                   | Comprimento de sal de 128 bits pode ser definido.<br/> |
| Algoritmo de criptografia de fluxo RC4                                                          | 40 bits                  | 128 bits                   | Comprimento de sal de 128 bits pode ser definido.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*DES triplo*](../secgloss/t-gly.md) (2 chaves) | Sem suporte            | 112 bits                   | 112 bits                                    |
| DES triplo (3 chaves)                                                                       | Sem suporte            | 168 bits                   | 168 bits                                    |



 

Para ver uma lista completa dos algoritmos com suporte, consulte [Algoritmos do provedor AES](aes-provider-algorithms.md).

O Provedor Forte, o Provedor Aprimorado e o Provedor AES são compatíveis com versões anteriores com o Provedor Base, exceto que os provedores podem gerar apenas chaves RC2 ou RC4 de comprimento de chave padrão. O comprimento padrão para o Provedor Base é de 40 bits. O comprimento padrão para o Provedor AES é de 128 bits. Portanto, o Provedor AES não pode criar chaves com comprimentos de chave compatíveis com o provedor base. No entanto, o Provedor AES pode importar chaves RC2 e RC4 de até 128 bits. Portanto, o Provedor AES pode importar e usar chaves de 40 bits geradas usando o Provedor Base.

 

 
