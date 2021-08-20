---
description: O provedor base e o provedor estendido usam os mesmos BLOBs de chave.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: BLOBs de chave do provedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95eaeaa1b6438045ebba55d2bb45785e4068154ff51818e937bc434dff7fb29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773038"
---
# <a name="base-provider-key-blobs"></a>BLOBs de chave do provedor base

O provedor base e o provedor estendido usam os mesmos [*blobs de chave*](../secgloss/k-gly.md).

-   [BLOBs de chave pública](#public-key-blobs)
-   [BLOBs de chave privada](#private-key-blobs)
-   [BLOBs de chave simples](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOBs de chave pública

Os [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para armazenar [*chaves públicas*](../secgloss/p-gly.md) fora de um [*provedor de serviços de criptografia*](../secgloss/c-gly.md) (CSP). Os BLOBs de chave pública do provedor base têm o seguinte formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

A tabela a seguir descreve cada componente de chave pública. Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .



| Campo          | Descrição                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| módulo        | Os dados do módulo de chave pública estão localizados diretamente após a estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . O tamanho desses dados irá variar, dependendo do tamanho da chave pública. O número de bytes pode ser determinado pela divisão do valor do campo **RSAPUBKEY bitlen** por oito. |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                 |
| rsapubkey      | Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . O membro **mágico** deve ser definido como 0x31415352. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA1.                                                                         |



 

> [!Note]  
> Os BLOBs de chave pública não são criptografados. Elas contêm chaves públicas em formato de [*texto sem formatação*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>BLOBs de chave privada

Os [*blobs de chave privada*](../secgloss/p-gly.md), o tipo **PRIVATEKEYBLOB**, são usados para armazenar [*chaves privadas*](../secgloss/p-gly.md) fora de um CSP. Os BLOBs de chave privada do provedor base têm o seguinte formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

A tabela a seguir descreve o componente BLOB de chave privada.

> [!Note]  
> Esses campos correspondem aos campos descritos na seção 7,2 de [*padrões de criptografia de chave pública*](../secgloss/p-gly.md) (PKCS) \# 1 com pequenas diferenças.

 



| Campo           | Descrição                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| cujo     | Cujo. Isso tem um valor numérico de (inverso de q) mod p.                                                                                                                                                |
| exponent1       | Expoente 1. Isso tem um valor numérico de d mod (p – 1).                                                                                                                                                        |
| exponent2       | Expoente 2. Isso tem um valor numérico de d mod (q – 1).                                                                                                                                                        |
| Modulus         | O módulo. Isso tem um valor de *Prime1*×*Prime2* e geralmente é conhecido como n.                                                                                                                                   |
| prime1          | Número principal 1, geralmente conhecido como p.                                                                                                                                                                             |
| prime2          | Número principal 2, geralmente conhecido como q.                                                                                                                                                                             |
| privateExponent | Expoente privado, geralmente conhecido como d.                                                                                                                                                                           |
| publickeystruc  | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| rsapubkey       | Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . O membro **mágico** deve ser definido como 0x32415352. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> Os BLOBs de chave privada não são criptografados. Eles contêm chaves privadas em formato de texto sem formatação.

 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave. O **PRIVATEKEYBLOB** será criptografado se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão. Tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada.

> [!Note]  
> Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada. O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.

 

> [!Caution]  
> É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

## <a name="simple-key-blobs"></a>BLOBs de chave simples

[*Blobs de chave simples*](../secgloss/s-gly.md), tipo **SIMPLEBLOB**, são usados para armazenar e transportar chaves de sessão fora de um CSP. Os BLOBs de chave simples do provedor base são sempre criptografados com uma [*chave pública de troca de chaves*](../secgloss/k-gly.md). O membro **pbData** do **SIMPLEBLOB** é uma sequência de bytes no formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

A tabela a seguir descreve cada componente do membro **pbData** do **SIMPLEBLOB**.



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Uma estrutura de [**\_ ID alg**](alg-id.md) que especifica o algoritmo de criptografia usado para criptografar os dados de chave de sessão. Normalmente, isso tem um valor de CALG \_ RSA \_ KEYX, que indica que os dados de chave de sessão foram criptografados com uma chave pública de troca de chaves usando o [*algoritmo de chave pública RSA*](../secgloss/r-gly.md).                                                                                                                           |
| EncryptedKey   | Uma sequência de **bytes** que representa os dados de chave de sessão criptografados na forma de um \# bloco de criptografia PKCS 1, tipo 2. Para obter informações sobre esse formato de dados, consulte os padrões de criptografia de chave pública (PKCS) \# 1, publicados pelo RSA Data Security, Inc. Esses dados são sempre do mesmo tamanho que o módulo da chave pública. Por exemplo, as chaves públicas geradas pelo provedor de base RSA da Microsoft podem ter 512 bits (64 bytes) de comprimento, de modo que os dados de chave de sessão criptografados também são sempre 512 bits (64 bytes).<br/> |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
