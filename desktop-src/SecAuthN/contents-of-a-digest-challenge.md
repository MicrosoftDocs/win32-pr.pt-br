---
description: O tamanho de um desafio de Acesso Digest deve ser menor que 2048 bytes.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Conteúdo de um desafio digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0f6ee840e4965ff9615052b57102409a977e5a90660772e963eaf06eb9875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883156"
---
# <a name="contents-of-a-digest-challenge"></a>Conteúdo de um desafio digest

O tamanho de um desafio de Acesso Digest deve ser menor que 2048 bytes. O exemplo a seguir mostra um desafio atribuído à cadeia de caracteres szChallenge.


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> A cadeia de caracteres de desafio é entre aspas duplas e contém aspas duplas inseridas. Aspas duplas inseridas devem ser precedidas (com escape) com uma faixa invertida ( \\ ).

 

Um desafio digest pode conter as diretivas a seguir.



| Diretiva         | Descrição                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reino             | Uma dica definida pela implementação para o cliente sobre quais [*credenciais*](/windows/desktop/SecGloss/c-gly) são necessárias. O cliente deverá exibir essas informações para o usuário se estiver solicitando credenciais.                                                  |
| algoritmo         | Microsoft Digest dá suporte a MD5 e MD5-Sess. Para obter um desempenho ideal, use MD5-Sess.                                                                                                                                                                                                                     |
| qop               | Essa diretiva pode ser definida como auth, auth-int ou auth-conf. Para obter mais informações, [consulte Qualidade de proteção e codificações.](quality-of-protection-and-ciphers.md)                                                                                                                                       |
| nonce             | Um valor codificado exclusivo gerado pelo servidor para cada desafio. Esse valor não deve ser alterado pelo cliente.                                                                                                                                                                                       |
| Opaco            | Contém uma referência para o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) que está sendo estabelecido. Para obter mais informações, consulte [Mantendo o contexto de segurança entre conexões](maintaining-the-security-context-between-connections.md). |
| cipher(somente SASL) | A lista de codificações compatíveis com o servidor. Esse elemento poderá estar presente em um desafio SASL digest somente se a diretiva qop especificar auth-conf. Para obter mais informações, [consulte Qualidade de proteção e codificações.](quality-of-protection-and-ciphers.md)                                              |
| charset           | Essa diretiva poderá ser definida como utf-8 se o servidor puder processar nomes de usuário codificados em UTF-8 e realms. Se o cliente entender a diretiva charset, ele poderá responder usando valores codificados em UTF-8.                                                                                                       |



 

Microsoft Digest gera a cadeia de caracteres de desafio digest para aplicativos de servidor. Para obter detalhes, [consulte Gerando o Desafio digest](generating-the-digest-challenge.md).

 

 
