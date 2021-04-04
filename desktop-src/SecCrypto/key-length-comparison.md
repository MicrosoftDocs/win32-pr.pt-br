---
description: O provedor criptográfico aprimorado da Microsoft fornece um aplicativo com segurança mais forte do que o que está disponível atualmente com o provedor Microsoft Base Cryptographic. O maior comprimento de chave oferece aos usuários mais proteção para dados confidenciais.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparação de comprimento de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837386"
---
# <a name="key-length-comparison"></a>Comparação de comprimento de chave

O provedor criptográfico aprimorado da Microsoft fornece um aplicativo com segurança mais forte do que o que está disponível atualmente com o provedor Microsoft Base Cryptographic. O maior comprimento de chave oferece aos usuários mais proteção para dados confidenciais.

A tabela a seguir lista os [*comprimentos de chave*](../secgloss/k-gly.md) padrão com suporte pelo provedor de base e o provedor avançado para algoritmos padrão.



| Algoritmo                                                                                | Provedor base | Provedores fortes e avançados |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| Troca de chaves RSA                                                                         | 512 bits       | 1.024 bits                     |
| Assinatura RSA                                                                            | 512 bits       | 1.024 bits                     |
| RC2                                                                                      | 40 bits        | 128 bits                       |
| RC4                                                                                      | 40 bits        | 128 bits                       |
| DES                                                                                      | Sem suporte | 56 bits                        |
| [*Des triplo*](../secgloss/t-gly.md) (2 teclas) | Sem suporte | 112 bits                       |
| DES triplo (3 teclas)                                                                       | Sem suporte | 168 bits                       |



 

Há suporte para algoritmos [*des*](../secgloss/d-gly.md) e [*Triple DES*](../secgloss/t-gly.md) no provedor avançado.

O provedor avançado é compatível com versões anteriores com o provedor de base distribuído com a versão anterior do CryptoAPI com a seguinte exceção. O provedor base e o provedor avançado só podem gerar chaves de sessão de comprimento de chave padrão. O comprimento padrão das chaves de sessão para o provedor de base é de 40 bits. O comprimento de chave padrão para o provedor avançado é de 128 bits. O provedor avançado não pode criar chaves com comprimentos de chave compatíveis com o provedor base. No entanto, o provedor avançado pode importar comprimentos de chave de qualquer tamanho, até 128 bits.

 

 
