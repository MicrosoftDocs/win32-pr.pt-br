---
description: O material a seguir é válido somente quando Digest é usado como um mecanismo SASL. Codificações e criptografia não estão disponíveis para autenticação HTTP usando Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Criptografias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165236"
---
# <a name="ciphers"></a>Criptografias

O material a seguir é válido somente quando Digest é usado como um mecanismo SASL. Codificações e criptografia não estão disponíveis para autenticação HTTP usando Microsoft Digest.

A diretiva de codificação de um desafio do Digest SASL contém uma lista das codificações com suporte de um servidor que exige comunicações confidenciais. A diretiva Cipher só poderá ser incluída se a diretiva QoP estiver definida como "auth-conf". As codificações reconhecidas pelo Microsoft Digest estão listadas na tabela a seguir, de forma mais forte para mais fraca.



| Valor de codificação | Descrição                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RC4        | A codificação RC4 com uma chave de 128 bits.                                                                                                                                                                                                                                                             |
| 3DES       | O [*Triple DES*](/windows/desktop/SecGloss/t-gly) Cipher no modo [*CBC*](/windows/desktop/SecGloss/c-gly) com ede com a mesma chave para cada estágio E (modo de duas chaves). O comprimento total da chave é de 112 bits. |
| "RC4-56"     | A codificação RC4 com uma chave de 56 bits.                                                                                                                                                                                                                                                              |
| "RC4-40"     | A codificação RC4 com uma chave de 40 bits.                                                                                                                                                                                                                                                              |
| des        | A criptografia des ( [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) ) no modo CBC ( [*encadeamento de blocos de codificação*](/windows/desktop/SecGloss/c-gly) ) com uma chave de 56 bits. |



 

Quando um aplicativo de servidor solicita confidencialidade (QoP = "auth-conf") Microsoft Digest gerará um desafio que oferece ao cliente todas as codificações instaladas no servidor e com suporte do resumo. O cliente Digest selecionará a codificação mais forte disponível. Para obter detalhes sobre como especificar a confidencialidade, consulte [gerando o desafio Digest](generating-the-digest-challenge.md).

 

 
