---
description: Os BLOBs são usados com o provedor RSA/Schannel para exportar chaves de e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: BLOBs de chave RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be8bfa8b87ee901317e220583ff7b08ea110e342a2d9dd9abb477053ffdf05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900531"
---
# <a name="rsaschannel-key-blobs"></a>BLOBs de chave RSA/Schannel

Os [*BLOBs*](../secgloss/b-gly.md) são usados com [](../secgloss/r-gly.md)o provedor de / [*Schannel*](../secgloss/s-gly.md) RSA para exportar chaves de e importar chaves para o CSP (provedor de [*serviços de criptografia*](../secgloss/c-gly.md) ).

-   [BLOBs de chave pública](#public-key-blobs)
-   [BLOBs de chave privada](#private-key-blobs)
-   [BLOBs de chave simples](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOBs de chave pública

Os [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para armazenar [*chaves públicas*](../secgloss/p-gly.md). Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

A tabela a seguir descreve cada componente de chave pública. Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .



| Campo          | Descrição                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| módulo        | Uma sequência de **bytes** . Os dados do módulo de chave pública estão localizados diretamente após a estrutura **RSAPUBKEY** . O comprimento desses dados varia, dependendo do comprimento da chave pública. O número de bytes pode ser determinado pela divisão do valor do membro **bitlen** de **RSAPUBKEY** por oito. |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                              |
| rsapubkey      | Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . O membro **mágico** deve ser definido como 0x31415352. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA1.                                                                                      |



 

> [!Note]  
> Os BLOBs de chave pública não são criptografados. Elas contêm chaves públicas em formato de [*texto sem formatação*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>BLOBs de chave privada

Os [*blobs de chave privada*](../secgloss/p-gly.md), o tipo **PRIVATEKEYBLOB**, são usados para armazenar [*pares de chaves pública/privada*](../secgloss/p-gly.md). Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

Se o [*blob de chave*](../secgloss/k-gly.md) for criptografado, tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob será criptografada.

> [!Note]  
> Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada. É responsabilidade do aplicativo gerenciar essas informações.

 

A tabela a seguir descreve cada componente de BLOB de chave privada.

> [!Note]  
> Esses campos correspondem aos campos descritos na seção 7,2 de [*padrões de criptografia de chave pública*](../secgloss/p-gly.md) (PKCS) \# 1 com pequenas diferenças.

 



| Campo           | Descrição                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | Uma sequência de **bytes** . O primeiro expoente. Isso tem um valor numérico de d mod (p – 1).                                                                                                                           |
| exponent2       | Uma sequência de **bytes** . O segundo expoente. Isso tem um valor numérico de d mod (q – 1).                                                                                                                          |
| cujo     | Uma sequência de **bytes** . Cujo. Isso tem um valor numérico de (inverso de q) mod p.                                                                                                                           |
| Modulus         | Uma sequência de **bytes** . O módulo. Isso tem uma cadeia de caracteres que contém *Prime1* \* *Prime2*. Geralmente é conhecido como n.                                                                                               |
| prime1          | Uma sequência de **bytes** . Número principal 1, geralmente conhecido como p.                                                                                                                                                        |
| prime2          | Uma sequência de **bytes** . Número principal 2, geralmente conhecido como q.                                                                                                                                                        |
| publickeystruc  | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| privateExponent | Uma sequência de **bytes** . O expoente privado, geralmente conhecido como d.                                                                                                                                                  |
| rsapubkey       | Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . O membro **mágico** deve ser definido como 0x32415352. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> Os BLOBs de chave privada não são criptografados. Eles contêm chaves privadas em formato de texto sem formatação.

 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave. O **PRIVATEKEYBLOB** será criptografado se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão. Tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada.

> [!Note]  
> Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada. O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.

 

> [!Caution]  
> É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

## <a name="simple-key-blobs"></a>BLOBs de chave simples

[*Blobs de chave simples*](../secgloss/s-gly.md), tipo **SIMPLEBLOB**, são usados para armazenar e transportar chaves de sessão. Eles são sempre criptografados com uma [*chave pública de troca de chaves*](../secgloss/k-gly.md). Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

A tabela a seguir descreve cada componente de BLOB simples.



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Uma estrutura de [**\_ ID alg**](alg-id.md) . Isso normalmente especifica o \_ algoritmo CALG RSA \_ KEYX, que indica que os dados de chave de sessão foram criptografados com uma chave pública de troca de chaves, usando o [*algoritmo de chave pública RSA*](../secgloss/r-gly.md). |
| EncryptedKey   | Uma sequência de **bytes** . Os dados de chave de sessão criptografada estão na forma de um \# bloco de criptografia PKCS 1, tipo 2. Para obter informações sobre esse formato de dados, consulte os padrões de criptografia de chave pública (PKCS), publicados pelo RSA Data Security, Inc.                                                                                     |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                         |



 

Esses dados são sempre do mesmo tamanho que o módulo da chave pública. Por exemplo, as chaves públicas geradas pelo provedor Microsoft Base Cryptographic são sempre 512 bits (64 bytes), portanto, os dados de chave de sessão criptografados também são sempre 64 bytes.

 

 
