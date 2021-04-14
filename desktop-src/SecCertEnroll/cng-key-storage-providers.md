---
description: 'Ao contrário da CryptoAPI (API de criptografia), a CNG (Cryptography API: Next Generation) separa os provedores criptográficos dos KSPs (provedores de armazenamento de chaves).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Provedores de armazenamento de chaves CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370592"
---
# <a name="cng-key-storage-providers"></a>Provedores de armazenamento de chaves CNG

Ao contrário da CryptoAPI (API de criptografia), a CNG (Cryptography API: Next Generation) separa os provedores criptográficos dos KSPs (provedores de armazenamento de chaves). KSPs pode ser usado para criar, excluir, exportar, importar, abrir e armazenar chaves. Dependendo da implementação, eles também podem ser usados para criptografia assimétrica, contrato secreto e assinatura. A Microsoft instala o seguinte KSPs a partir do Windows Vista e do Windows Server 2008. Os fornecedores podem criar e instalar outros provedores.

## <a name="microsoft-software-key-storage-provider"></a>Provedor de armazenamento de chaves de software da Microsoft

Dá suporte à criação de chave de software e ao armazenamento e aos seguintes algoritmos.



| Algoritmo                                          | Finalidade                           | Comprimento da chave (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Acordo de segredo e troca de chaves | 512 a 4096 em incrementos de bits 64  |
| Algoritmo de assinatura digital (DSA)                  | Assinaturas                        | 512 a 1024 em incrementos de bits 64  |
| Diffie-Hellman de curva elíptica (ECDH)               | Acordo de segredo e troca de chaves | P256, P384, P521                  |
| ECDSA (algoritmo de assinatura digital de curva elíptica) | Assinaturas                        | P256, P384, P521                  |
| RSA                                                | Criptografia assimétrica e assinatura | 512 a 16384 em incrementos de bits 64 |



 

## <a name="microsoft-smart-card-key-storage-provider"></a>Provedor de armazenamento de chaves de cartão inteligente da Microsoft

Dá suporte à criação e ao armazenamento de chave de cartão inteligente e aos seguintes algoritmos.



| Algoritmo                                          | Finalidade                           | Comprimento da chave (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Acordo de segredo e troca de chaves | 512 a 4096 em incrementos de bits 64  |
| Diffie-Hellman de curva elíptica (ECDH)               | Acordo de segredo e troca de chaves | P256, P384, P521                  |
| ECDSA (algoritmo de assinatura digital de curva elíptica) | Assinaturas                        | P256, P384, P521                  |
| RSA                                                | Criptografia assimétrica e assinatura | 512 a 16384 em incrementos de bits 64 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funções de armazenamento de chaves CNG](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[Noções básicas sobre provedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
