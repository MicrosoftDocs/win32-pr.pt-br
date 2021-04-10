---
description: O tamanho de um desafio de acesso de resumo deve ser inferior a 2048 bytes.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Conteúdo de um desafio de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089954"
---
# <a name="contents-of-a-digest-challenge"></a>Conteúdo de um desafio de resumo

O tamanho de um desafio de acesso de resumo deve ser inferior a 2048 bytes. O exemplo a seguir mostra um desafio atribuído à cadeia de caracteres szChallenge.


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> A cadeia de caracteres de desafio é colocada entre aspas duplas e contém aspas duplas inseridas. Aspas duplas inseridas devem ser precedidas (escape) com uma barra invertida ( \\ ).

 

Um desafio de resumo pode conter as seguintes diretivas.



| Diretiva         | Descrição                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| territórios             | Uma dica definida pela implementação para o cliente sobre quais [*credenciais*](/windows/desktop/SecGloss/c-gly) são necessárias. O cliente deve exibir essas informações para o usuário se ele estiver solicitando credenciais.                                                  |
| algoritmo         | Microsoft Digest dá suporte a MD5 e MD5-sess. Para obter um desempenho ideal, use MD5-sess.                                                                                                                                                                                                                     |
| qop               | Essa diretiva pode ser definida como auth, auth-int ou auth-conf. Para obter mais informações, consulte [qualidade de proteção e codificações](quality-of-protection-and-ciphers.md).                                                                                                                                       |
| nonce             | Um valor codificado exclusivo gerado pelo servidor para cada desafio. Esse valor não deve ser alterado pelo cliente.                                                                                                                                                                                       |
| opaco            | Contém uma referência para o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) que está sendo estabelecido. Para obter mais informações, consulte [mantendo o contexto de segurança entre conexões](maintaining-the-security-context-between-connections.md). |
| cipher (somente SASL) | A lista de codificações às quais o servidor dá suporte. Esse elemento pode estar presente em um desafio de Digest SASL somente se a diretiva QoP especifica auth-conf. Para obter mais informações, consulte [qualidade de proteção e codificações](quality-of-protection-and-ciphers.md).                                              |
| charset           | Essa diretiva pode ser definida como UTF-8 se o servidor puder processar nomes de usuário e territórios codificados em UTF-8. Se o cliente compreender a diretiva charset, ele poderá responder usando valores codificados em UTF-8.                                                                                                       |



 

Microsoft Digest gera a cadeia de caracteres de desafio Digest para aplicativos de servidor. Para obter detalhes, consulte [gerando o desafio Digest](generating-the-digest-challenge.md).

 

 
