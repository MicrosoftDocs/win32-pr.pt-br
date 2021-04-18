---
description: Os algoritmos podem ter suporte do provedor criptográfico Microsoft RSA/Schannel.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algoritmos de provedor RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778671"
---
# <a name="rsaschannel-provider-algorithms"></a>Algoritmos de provedor RSA/Schannel

Os algoritmos a seguir podem ser suportados pelo provedor Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) Cryptographic.



| ID do algoritmo    | Descrição                                                                                                                         | Comentários                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ RSA \_ KEYX | [ *Algoritmo de troca de chave* de chave pública RSA](../secgloss/k-gly.md) | Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits. Comprimento de chave padrão: 1.024 bits.<br/> |
| CALG \_ MD5       | Algoritmo de hash MD5.                                                                                                              | Fornecido somente para hash.                                                                                      |
| CALG \_ Sha       | Algoritmo de hash SHA.                                                                                                              | Deve ser usado para assinaturas DSS.                                                                                |
| CALG \_ RC2       | Algoritmo de criptografia de bloco RC2.                                                                                                     | Comprimento da chave: 40 a 88 bits                                                                                       |
| CALG \_ RC4       | Algoritmo de criptografia de fluxo RC4.                                                                                                    | Comprimento da chave: 40 a 88 bits                                                                                       |



 

 

 
