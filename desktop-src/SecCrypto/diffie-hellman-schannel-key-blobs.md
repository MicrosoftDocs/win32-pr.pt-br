---
description: BLOBs são usados com o provedor Diffie-Hellman/Schannel para exportar chaves e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: BLOBs de Chaves Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c653e26f53611e8b00a1dae4e49df7084e6dc655d67f11550a430860fab12d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767690"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>BLOBs de Chaves Diffie-Hellman/Schannel

[*BLOBs*](../secgloss/b-gly.md) são usados com o provedor [*Schannel Diffie-Hellman*](../secgloss/d-gly.md)para exportar chaves e importar chaves para o CSP (provedor de serviços de / [](../secgloss/s-gly.md) criptografia). [](../secgloss/c-gly.md)

-   [BLOBs de Chave Pública](#public-key-blobs)
-   [BLOBs de Chave Privada](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOBs de Chave Pública

Diffie-Hellman [*BLOBs*](../secgloss/p-gly.md)de chave pública , tipo **PUBLICKEYBLOB**, são usados para trocar o valor P mod (G^X) em uma Diffie-Hellman troca de chaves. Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

A tabela a seguir descreve cada componente do [*BLOB de chaves.*](../secgloss/k-gly.md)



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Uma [**estrutura DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) O **membro** mágico deve ser definido como 0x31484400. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Uma [**estrutura PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a              | Uma **sequência de BYTE.** O valor y, (G^X) mod P, está localizado diretamente após a [**estrutura DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) O comprimento, em bytes, da sequência é o **membro bitlen** **de DHPUBKEY** dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G^X) mod P for um ou mais bytes mais curtos do que P dividido por oito, os dados deverão ser alojados com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado [*(formato little-endian).*](../secgloss/l-gly.md) |



 

## <a name="private-key-blobs"></a>BLOBs de Chave Privada

[*BLOBs*](../secgloss/p-gly.md)de chave privada D-H , tipo **PRIVATEKEYBLOB**, são usados para exportar e importar informações privadas de uma chave D-H. Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

A tabela a seguir descreve cada componente do BLOB de chaves.



| Campo          | Descrição                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Uma [**estrutura DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) O **membro** mágico deve ser definido como 0x32484400. Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DH2. |
| gerador      | Uma **sequência de BYTE.** O gerador G.                                                                                                                                                                      |
| publickeystruc | Uma [**estrutura PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                      |
| Principal          | Uma **sequência de BYTE.** O módulo principal, P. Esses dados sempre devem ter o bit mais significativo do byte mais significativo definido como um.                                                                    |
| segredo         | Uma **sequência de BYTE.** O expoente secreto X.                                                                                                                                                                |



 

> [!Note]  
> Os valores principal, gerador e segredo devem sempre ter o mesmo comprimento, em bytes. Se qualquer valor for um byte ou mais curto do que os outros, ele deverá ser preenchimento com o número necessário de zero bytes para torná-los iguais. O principal, o gerador e o segredo estão no [*formato little endian.*](../secgloss/l-gly.md)

 

 

 
