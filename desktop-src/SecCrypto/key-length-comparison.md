---
description: O Provedor criptográfico aprimorado da Microsoft fornece um aplicativo com segurança mais forte do que o disponível atualmente com o Provedor criptográfico da Microsoft Base. Maior comprimento de chave oferece aos usuários mais proteção para dados confidenciais.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparação de comprimento de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65615f6ffb9679b922600c4617e401067d565ac7dd62a258ae07a757d2cec7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622341"
---
# <a name="key-length-comparison"></a>Comparação de comprimento de chave

O Provedor criptográfico aprimorado da Microsoft fornece um aplicativo com segurança mais forte do que o disponível atualmente com o Provedor criptográfico da Microsoft Base. Maior comprimento de chave oferece aos usuários mais proteção para dados confidenciais.

A tabela a seguir lista os [*comprimentos de*](../secgloss/k-gly.md) chave padrão com suporte pelo Provedor Base e pelo Provedor Avançado para algoritmos padrão.



| Algoritmo                                                                                | Provedor base | Provedores fortes e aprimorados |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| Chave RSA Exchange                                                                         | 512 bits       | 1.024 bits                     |
| Assinatura RSA                                                                            | 512 bits       | 1.024 bits                     |
| RC2                                                                                      | 40 bits        | 128 bits                       |
| RC4                                                                                      | 40 bits        | 128 bits                       |
| DES                                                                                      | Sem suporte | 56 bits                        |
| [*DES triplo*](../secgloss/t-gly.md) (2 chaves) | Sem suporte | 112 bits                       |
| DES triplo (3 chaves)                                                                       | Sem suporte | 168 bits                       |



 

[*Os algoritmos DES*](../secgloss/d-gly.md) e [*TRIPLE DES*](../secgloss/t-gly.md) têm suporte no Provedor Avançado.

O Provedor Aprimorado é compatível com versões anteriores com o Provedor Base distribuído com versões anteriores do CryptoAPI com a exceção a seguir. O provedor base e o Provedor Aprimorado só podem gerar chaves de sessão de comprimento de chave padrão. O comprimento padrão das chaves de sessão para o Provedor Base é de 40 bits. O comprimento da chave padrão para o Provedor Aprimorado é de 128 bits. O Provedor Aprimorado não pode criar chaves com comprimentos de chave compatíveis com o Provedor Base. No entanto, o Provedor Aprimorado pode importar comprimentos de chave de qualquer tamanho, até 128 bits.

 

 
