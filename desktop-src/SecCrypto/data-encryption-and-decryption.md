---
description: Criptografia é o processo de conversão de dados de texto sem formatação (texto não criptografado) em algo que pareça aleatório e sem sentido (texto cifrado). A descriptografia é o processo de converter o texto cifrado de volta em texto não criptografado.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Criptografia e descriptografia de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090192"
---
# <a name="data-encryption-and-decryption"></a>Criptografia e descriptografia de dados

Criptografia é o processo de conversão de dados de texto sem formatação (texto não [*criptografado*](../secgloss/p-gly.md)) em algo que pareça aleatório e sem sentido ([*texto cifrado*](../secgloss/c-gly.md)). A descriptografia é o processo de converter o texto cifrado de volta em texto não criptografado.

Para criptografar mais de uma pequena quantidade de dados, a [*criptografia simétrica*](../secgloss/s-gly.md) é usada. Uma [*chave simétrica*](../secgloss/s-gly.md) é usada durante os processos de criptografia e descriptografia. Para descriptografar uma parte específica do texto cifrado, a chave que foi usada para criptografar os dados deve ser usada.

A meta de cada algoritmo de criptografia é torná-lo o mais difícil possível de descriptografar o texto cifrado gerado sem usar a chave. Se um algoritmo de criptografia realmente bom for usado, não há nenhuma técnica significativamente melhor do que tentar cada chave de maneira metódica. Para esse algoritmo, quanto mais longa for a chave, mais difícil será descriptografar uma parte do texto cifrado sem possuir a chave.

É difícil determinar a qualidade de um algoritmo de criptografia. Os algoritmos que parecem promissores, às vezes, são muito fáceis de quebrar, devido ao ataque adequado. Ao selecionar um algoritmo de criptografia, é uma boa ideia escolher um que tenha sido usado por vários anos e que tenha reparado com êxito todos os ataques.

Para obter mais informações, consulte [funções de criptografia e](cryptography-functions.md)descriptografia de dados.

 

 
