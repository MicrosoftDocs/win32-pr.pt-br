---
description: A API CNG fornece um conjunto de funções que executam operações de criptografia básicas, como a criação de hashes ou a criptografia e a descriptografia de dados. Para obter mais informações sobre essas funções, consulte funções primitivas de criptografia CNG.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Primitivos criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501260"
---
# <a name="cryptographic-primitives"></a>Primitivos criptográficos

A API CNG fornece um conjunto de funções que executam operações de criptografia básicas, como a criação de hashes ou a criptografia e a descriptografia de dados. Para obter mais informações sobre essas funções, consulte [funções primitivas de criptografia CNG](cng-cryptographic-primitive-functions.md).

A CNG implementa vários algoritmos criptográficos. Cada algoritmo ou classe de algoritmos expõe sua própria API primitiva. Várias implementações de um determinado algoritmo podem ser instaladas ao mesmo tempo; no entanto, apenas uma implementação será o padrão em um determinado momento.

Cada classe de algoritmo na CNG é representada por um roteador primitivo. Os aplicativos que usam as funções do CNG primitiva serão vinculados ao arquivo binário do roteador Bcrypt.dll no modo de usuário ou Ksecdd.sys no modo kernel antes de chamar as funções. Várias rotinas de roteador gerenciam todos os primitivos de algoritmo. Esses roteadores rastreiam cada implementação de algoritmo instalada no sistema e roteiam cada chamada de função para o módulo de provedor primitivo apropriado.

A CNG fornece primitivos para as seguintes classes de algoritmos.



| Classe de algoritmo                                                                                                                                                  | Descrição                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Gerador de número aleatório<br/> | Geração de número aleatório conectável (RNG).<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hash<br/>                                                                 | Algoritmos usados para hash, como SHA1 e SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Criptografia simétrica<br/>             | Algoritmos usados para criptografia simétrica, como AES, 3DES e RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Criptografia assimétrica<br/>         | Algoritmos assimétricos (chave pública) que dão suporte à criptografia, como RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature<br/>                                                         | Algoritmos de assinatura como DSA e ECDSA. Essa classe também pode ser usada com RSA.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Contrato secreto<br/>                             | Algoritmos de contrato secreto, como Diffie-Hellman (DH) e Diffie-Hellman de curva elíptica (ECDH).<br/> |



 

A ilustração a seguir mostra o design e a função dos primitivos de criptografia CNG.

![Design e função de primitivos criptográficos CNG](images/ssdk-cng1c.png)

O arquivo de cabeçalho bcrypt. h define a constante do **\_ \_ provedor de MS Primitive** como "provedor Microsoft Primitive". Para usar o provedor Microsoft Primitive, passe esse valor para [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




