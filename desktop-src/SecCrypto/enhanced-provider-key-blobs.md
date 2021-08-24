---
description: O Provedor Base, o Provedor Forte e o Provedor Aprimorado usam os mesmos BLOBs de chave.
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: BLOBs de chaves do provedor aprimorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1098ec45f73183f31cb91d15e2957dcc5964591bd8c6de4e30616df0808ade6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874436"
---
# <a name="enhanced-provider-key-blobs"></a>BLOBs de chaves do provedor aprimorados

O Provedor Base, o Provedor Forte e o Provedor Aprimorado usam os mesmos [*BLOBs de chave.*](../secgloss/k-gly.md)

-   [BLOBs de Chave Pública](#public-key-blobs)
-   [BLOBs de Chave Privada](#private-key-blobs)
-   [BLOBs de Chaves Simples](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOBs de Chave Pública

[*BLOBs de chave*](../secgloss/p-gly.md)pública , tipo **PUBLICKEYBLOB**, são usados para armazenar chaves públicas [*fora*](../secgloss/p-gly.md) de um CSP (provedor de [*serviços de*](../secgloss/c-gly.md) criptografia). BLOBs de chave pública do provedor estendido têm o seguinte formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

A tabela a seguir descreve cada componente de chave pública. Todos os valores estão no [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descrição                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| módulo        | Os dados de módulo de chave pública estão localizados diretamente após a [**estrutura RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) O tamanho desses dados variará, dependendo do tamanho da chave pública. O número de bytes pode ser determinado dividindo o valor do **campo bitlen RSAPUBKEY** por oito. |
| publickeystruc | Uma [**estrutura PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                 |
| rsapubkey      | Uma [**estrutura RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) O **membro** mágico deve ser definido como 0x31415352. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA1.                                                                         |



 

> [!Note]  
> BLOBs de chave pública não são criptografados. Elas contêm chaves públicas em [*formato de texto não*](../secgloss/p-gly.md) criptografado.

 

## <a name="private-key-blobs"></a>BLOBs de Chave Privada

[*BLOBs de chave privada*](../secgloss/p-gly.md), tipo **PRIVATEKEYBLOB**, são usados para armazenar [*chaves privadas*](../secgloss/p-gly.md) fora de um CSP. BLOBs de chave privada do provedor estendido têm o seguinte formato.

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
> Esses campos correspondem aos campos descritos na seção 7.2 de PKCS (Public [*Key Cryptography Standards)*](../secgloss/p-gly.md) \# 1 com pequenas diferenças.

 



| Campo           | Descrição                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coeficiente     | Coeficiente. Isso tem um valor numérico de (inverso de q) mod p.                                                                                                                                                |
| exponent1       | Expoente 1. Isso tem um valor numérico de d mod (p – 1).                                                                                                                                                        |
| exponent2       | Expoente 2. Isso tem um valor numérico de d mod (q – 1).                                                                                                                                                        |
| Modulus         | O módulo. Isso tem um valor de *Prime1*×*Prime2* e geralmente é conhecido como n.                                                                                                                                   |
| prime1          | Número principal 1, geralmente conhecido como p.                                                                                                                                                                             |
| prime2          | Número principal 2, geralmente conhecido como q.                                                                                                                                                                             |
| privateExponent | Expoente privado, geralmente conhecido como d.                                                                                                                                                                           |
| publickeystruc  | Uma [**estrutura PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| rsapubkey       | Uma [**estrutura RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) O **membro** mágico deve ser definido como 0x32415352. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> BLOBs de chave privada não são criptografados. Elas contêm chaves privadas em formato de texto não criptografado.

 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deve criptografar a chave. O **PRIVATEKEYBLOB** será criptografado se o parâmetro *hExpKey* contiver um alçado válido para uma chave de sessão. Tudo, menos [**a parte PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do BLOB, é criptografado.

> [!Note]  
> O algoritmo de criptografia e os parâmetros de chave de criptografia não são armazenados junto com o BLOB de chave privada. O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey,* a chave privada será exportada sem criptografia.

 

> [!Caution]  
> É perigoso exportar chaves privadas sem criptografia porque elas ficam vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

## <a name="simple-key-blobs"></a>BLOBs de Chaves Simples

[*BLOBs de chaves simples*](../secgloss/s-gly.md), tipo **SIMPLEBLOB**, são usados para armazenar e transportar chaves de sessão fora de um CSP. BLOBs de chaves simples do provedor estendido são sempre criptografados com uma [*chave pública de troca de chaves*](../secgloss/k-gly.md). O **membro pbData** do **SIMPLEBLOB** é uma sequência de bytes no formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

A tabela a seguir descreve cada componente do membro **pbData** do **SIMPLEBLOB.**



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Algid          | Uma [**estrutura de \_ ID alg**](alg-id.md) que especifica o algoritmo de criptografia usado para criptografar os dados da chave de sessão. Normalmente, isso tem um valor de CALG RSA KEYX, que indica que os dados da chave de sessão foram criptografados com uma chave pública de troca de chaves usando o algoritmo chave pública \_ \_ [*RSA*](../secgloss/r-gly.md).                                                                                                                           |
| Encryptedkey   | Uma **sequência BYTE** que representa os dados de chave de sessão criptografada na forma de um bloco de criptografia PKCS \# 1, tipo 2. Para obter informações sobre esse formato de dados, consulte PKCS (Public Key Cryptography Standards) \# 1, publicado pela RSA Data Security, Inc. Esses dados sempre são do mesmo tamanho que o módulo da chave pública. Por exemplo, as chaves públicas geradas pelo Provedor Base de RSA da Microsoft podem ter 512 bits (64 bytes), portanto, os dados de chave de sessão criptografada também são sempre 512 bits (64 bytes).<br/> |
| publickeystruc | Uma [**estrutura PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Para obter informações sobre o provedor base e blobs de chaves do provedor estendido, consulte [BLOBs de chaves do provedor de base.](base-provider-key-blobs.md)

 

 
