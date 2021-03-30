---
description: Os BLOBs são usados com o provedor Diffie-Hellman/Schannel para exportar chaves e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: BLOBs de chave Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662167"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>BLOBs de chave Diffie-Hellman/Schannel

Os [*BLOBs*](../secgloss/b-gly.md) são usados com o provedor Schannel [*Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) para exportar chaves e importar chaves para o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).

-   [BLOBs de chave pública](#public-key-blobs)
-   [BLOBs de chave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOBs de chave pública

Diffie-Hellman [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para trocar o valor (G ^ X) mod P em uma troca de chaves Diffie-Hellman. Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

A tabela a seguir descreve cada componente do [*blob de chave*](../secgloss/k-gly.md).



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . O membro **mágico** deve ser definido como 0x31484400. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a              | Uma sequência de **bytes** . O valor y, (G ^ X) mod P, está localizado diretamente após a estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . O comprimento, em bytes, da sequência é o membro **bitlen** de **DHPUBKEY** dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por oito, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado ([*little-endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>BLOBs de chave privada

Os [*blobs de chave privada*](../secgloss/p-gly.md)D-H, digite **PRIVATEKEYBLOB**, são usados para exportar e importar informações privadas de uma chave D-h. Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

A tabela a seguir descreve cada componente do BLOB de chave.



| Campo          | Descrição                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . O membro **mágico** deve ser definido como 0x32484400. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DH2. |
| gerador      | Uma sequência de **bytes** . O gerador G.                                                                                                                                                                      |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                      |
| Trata          | Uma sequência de **bytes** . O principal módulo, P. Esses dados devem sempre ter o bit mais significativo do conjunto de bytes mais significativo para um.                                                                    |
| segredo         | Uma sequência de **bytes** . O expoente X do segredo.                                                                                                                                                                |



 

> [!Note]  
> Os valores primo, Generator e Secret devem sempre ter o mesmo comprimento, em bytes. Se qualquer valor for um byte ou mais curto do que os outros, ele deverá ser preenchido com o número necessário de zero bytes para torná-los iguais. O primo, o gerador e o segredo estão no formato [*little-endian*](../secgloss/l-gly.md) .

 

 

 
