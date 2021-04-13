---
description: A finalidade do algoritmo de Diffie-Hellman é possibilitar que dois ou mais hosts criem e compartilhem uma chave de criptografia secreta idêntica, simplesmente compartilhando informações em uma rede que não seja segura.
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Algoritmos de provedor Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4fb88e3a50e15a6690340ab3fbcee91da1193a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297677"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a>Algoritmos de provedor Diffie-Hellman/Schannel

A finalidade do algoritmo de Diffie-Hellman é possibilitar que dois ou mais hosts criem e compartilhem uma chave de criptografia secreta idêntica, simplesmente compartilhando informações em uma rede que não seja segura. As informações que são compartilhadas pela rede estão na forma de alguns valores constantes e uma chave pública D-H.

O provedor criptográfico Schannel do Microsoft [*Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) oferece suporte aos seguintes algoritmos.



| ID do algoritmo                  | Descrição                                                                                                                                           | Comentários                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| CALG \_ DH \_ it                  | Diffie-Hellman armazenar e encaminhar [ *algoritmo de troca de chaves*](../secgloss/k-gly.md) | Comprimento da chave: pode ser definido, 384 bits a 512 bits em incrementos de 8 bits. Comprimento de chave padrão: 512 bits.<br/> |
| CALG \_ MD5                     | Algoritmo de hash MD5.                                                                                                                                | Fornecido somente para hash.                                                                                 |
| CALG \_ DH \_ EPHEM               | Troca de chaves efêmeras D-H.                                                                                                                           | Comprimento da chave: pode ser definido, 384 bits a 512 bits em incrementos de 8 bits. Comprimento de chave padrão: 512 bits.<br/> |
| CALG \_ Sha                     | Algoritmo de hash SHA.                                                                                                                                | Deve ser usado para assinaturas DSS.                                                                           |
| CALG \_ RC2                     | Algoritmo de criptografia de bloco RC2                                                                                                                        | Comprimento da chave: 40 a 88 bits.                                                                                 |
| CALG \_ RC4                     | Algoritmo de criptografia de fluxo RC4                                                                                                                       | Comprimento da chave: 40 a 88 bits.                                                                                 |
| CALG \_ CYLINK \_ MEK<br/> | Algoritmo de criptografia de variante DES                                                                                                                      | Comprimento da chave: 40 bits.                                                                                       |



 

 

 
