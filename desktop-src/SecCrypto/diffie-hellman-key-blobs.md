---
description: Os BLOBs são usados com o provedor de Diffie-Hellman para exportar chaves e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: BLOBs de chave de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757475"
---
# <a name="diffie-hellman-key-blobs"></a>BLOBs de chave de Diffie-Hellman

Os [*BLOBs*](../secgloss/b-gly.md) são usados com o provedor [*Diffie-Hellman*](../secgloss/d-gly.md) para exportar chaves e importar chaves para o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).

-   [BLOBs de chave pública](#public-key-blobs)
-   [BLOBs de chave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOBs de chave pública

Diffie-Hellman [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para trocar o valor (G ^ X) mod P em uma troca de chaves Diffie-Hellman. Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

A tabela a seguir descreve cada componente do [*blob de chave*](../secgloss/k-gly.md).



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . O membro **mágico** deve ser definido como 0x31484400. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de "DH1".                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| a              | Uma sequência de **bytes** . O valor Y, (G ^ X) mod P, está localizado diretamente após a estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) e deve ser sempre o comprimento, em bytes, do campo **DHPUBKEY bitlen** (tamanho de bit P) dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por oito, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado ([*little-endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>BLOBs de chave privada

Diffie-Hellman [*blobs de chave privada*](../secgloss/p-gly.md), digite **PRIVATEKEYBLOB**, são usados para armazenar as informações públicas/privadas de uma chave de Diffie-Hellman. Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

A tabela a seguir descreve cada componente do BLOB de chave.



| Campo          | Descrição                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . O membro **mágico** deve ser definido como 0x32484400. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de "DH2". |
| gerador      | Uma sequência de **bytes** . O gerador, G.                                                                                                                                                                       |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                        |
| Trata          | Uma sequência de **bytes** . O principal módulo, P. Esses dados devem sempre ter o bit mais significativo do conjunto de bytes mais significativo para um.                                                                      |
| segredo         | Uma sequência de **bytes** . O expoente secreto, X.                                                                                                                                                                 |



 

> [!Note]  
> O gerador e o segredo devem sempre ter o mesmo comprimento, em bytes. Se for um byte ou mais curto do que o outro, ele deverá ser preenchido com o número necessário de bytes de valor zero para torná-los os mesmos. O gerador e o segredo estão no formato [*little-endian*](../secgloss/l-gly.md) .

 

 

 
