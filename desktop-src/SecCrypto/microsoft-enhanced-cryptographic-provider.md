---
description: O provedor criptográfico aprimorado da Microsoft oferece suporte aos mesmos recursos que o provedor Microsoft Base Cryptographic, mas dá suporte à segurança mais forte por meio de chaves mais longas e algoritmos adicionais.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Provedor criptográfico aprimorado da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf3b3b421e3151811da033e7536f334e3883487
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581824"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Provedor criptográfico aprimorado da Microsoft

O provedor criptográfico aprimorado da Microsoft, chamado provedor avançado, dá suporte aos mesmos recursos que o provedor Microsoft Base Cryptographic, chamado provedor base. O provedor avançado dá suporte à segurança mais forte por meio de chaves mais longas e algoritmos adicionais. Ele pode ser usado com todas as versões do CryptoAPI.

Para manter a compatibilidade com versões anteriores do provedor, o nome do provedor, conforme definido no arquivo de cabeçalho Wincrypt. h, retém a designação da versão 1,0. No entanto, a versão 2,0 deste provedor está sendo fornecida no momento. Para determinar a versão do provedor em uso, chame [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o argumento *DwParam* definido como **PP \_ version**. A versão 2,0 estará em uso se 0x0200 for retornado.

|                   | Valor               |
|-------------------|---------------------|
| **Tipo de provedor** | PROV \_ RSA \_ completo     |
| **Nome do provedor** | \_Prov aprimorado da MS \_  |



 

A tabela a seguir realça as diferenças entre o provedor base, o provedor forte e o provedor avançado. Os comprimentos de chave mostrados são os comprimentos de chave padrão.



| Algoritmo                                                                                | Comprimento da chave do provedor base | Comprimento da chave do provedor forte | Comprimento da chave do provedor avançado                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de assinatura de chave pública RSA                                                       | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de troca de chave pública RSA                                                        | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de criptografia de bloco RC2                                                           | 40 bits                  | 128 bits                   | o comprimento de Salt de 128 bits pode ser definido.<br/> |
| Algoritmo de criptografia de fluxo RC4                                                          | 40 bits                  | 128 bits                   | o comprimento de Salt de 128 bits pode ser definido.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Des triplo*](../secgloss/t-gly.md) (2 teclas) | Sem suporte            | 112 bits                   | 112 bits                                    |
| DES triplo (3 teclas)                                                                       | Sem suporte            | 168 bits                   | 168 bits                                    |



 

O provedor forte e o provedor avançado são compatíveis com versões anteriores com o provedor base, exceto que os provedores só podem gerar chaves RC2 ou RC4 de [*comprimento de chave*](../secgloss/k-gly.md)padrão. O comprimento padrão para o provedor de base é de 40 bits. O comprimento padrão para o provedor avançado é de 128 bits. Portanto, o provedor avançado não pode criar chaves com comprimentos de chave compatíveis com o provedor base. No entanto, o provedor avançado pode importar as chaves RC2 e RC4 de até 128 bits. Portanto, o provedor avançado pode importar e usar chaves de 40 bits geradas usando o provedor base.

 

 
