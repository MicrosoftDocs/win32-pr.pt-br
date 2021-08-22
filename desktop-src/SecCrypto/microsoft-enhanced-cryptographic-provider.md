---
description: O Provedor criptográfico avançado da Microsoft dá suporte aos mesmos recursos que o Provedor criptográfico da Microsoft Base, mas dá suporte à segurança mais forte por meio de chaves mais longas e algoritmos adicionais.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Provedor criptográfico aprimorado da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60dbe254f9f22623a61de51b044b58df3a52f19f8a0b4f283caba3f59db7974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425506"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Provedor criptográfico aprimorado da Microsoft

O Provedor criptográfico aprimorado da Microsoft, chamado de Provedor Aprimorado, dá suporte aos mesmos recursos que o Provedor de Criptografia Base da Microsoft, chamado de Provedor Base. O Provedor Avançado dá suporte à segurança mais forte por meio de chaves mais longas e algoritmos adicionais. Ele pode ser usado com todas as versões do CryptoAPI.

Para manter a compatibilidade com versões anteriores do provedor, o nome do provedor, conforme definido no arquivo de título Wincrypt.h, retém a designação da versão 1.0. No entanto, a versão 2.0 desse provedor está sendo remessada no momento. Para determinar a versão do provedor em uso, chame [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o *argumento dwParam* definido como **PP \_ VERSION.** A versão 2.0 está em uso se 0x0200 é retornado.

|                   | Valor               |
|-------------------|---------------------|
| **Tipo de provedor** | PROV \_ RSA \_ FULL     |
| **Nome do provedor** | PROV \_ APRIMORADO do MS \_  |



 

A tabela a seguir destaca as diferenças entre o Provedor Base, o Provedor Forte e o Provedor Aprimorado. Os comprimentos de chave mostrados são os comprimentos de chave padrão.



| Algoritmo                                                                                | Comprimento da chave do provedor base | Comprimento da chave do Provedor Forte | Comprimento de chave do provedor aprimorado                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de assinatura de chave pública RSA                                                       | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de troca de chaves públicas RSA                                                        | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de criptografia de bloco RC2                                                           | 40 bits                  | 128 bits                   | Comprimento de sal de 128 bits pode ser definido.<br/> |
| Algoritmo de criptografia de fluxo RC4                                                          | 40 bits                  | 128 bits                   | Comprimento de sal de 128 bits pode ser definido.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*DES triplo*](../secgloss/t-gly.md) (2 chaves) | Sem suporte            | 112 bits                   | 112 bits                                    |
| DES triplo (3 chaves)                                                                       | Sem suporte            | 168 bits                   | 168 bits                                    |



 

O Provedor Forte e o Provedor Aprimorado são compatíveis com versões anteriores com o Provedor Base, exceto que os provedores só podem gerar chaves RC2 ou RC4 de comprimento [*de chave padrão.*](../secgloss/k-gly.md) O comprimento padrão para o Provedor Base é de 40 bits. O comprimento padrão para o Provedor Aprimorado é de 128 bits. Portanto, o Provedor Aprimorado não pode criar chaves com comprimentos de chave compatíveis com o provedor base. No entanto, o Provedor Aprimorado pode importar chaves RC2 e RC4 de até 128 bits. Portanto, o Provedor Aprimorado pode importar e usar chaves de 40 bits geradas usando o Provedor Base.

 

 
