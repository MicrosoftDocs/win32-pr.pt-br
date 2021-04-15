---
description: Descreve o formato de um BLOB de chave privada da versão 3 Diffie-Hellman exportada.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: BLOBs de chave privada do Diffie-Hellman versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb35a6db0cfd75d34ba30d26be816a64c1b04205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461028"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>BLOBs de chave privada do Diffie-Hellman versão 3

Quando um blob de [*chave privada*](../secgloss/p-gly.md) Diffie-Hellman versão 3 é exportado, ele está em um formato da seguinte maneira:


```C++
BLOBHEADER        blobheader;
DHPRIVKEY_VER3   dhprivkeyver3;
BYTE p[dhprivkeyver3.bitlenP/8]; 
            // Where P is the prime modulus
BYTE q[dhprivkeyver3.bitlenQ/8]; 
            // Where Q is a large factor of P-1
BYTE g[dhprivkeyver3.bitlenP/8]; 
            // Where G is the generator parameter
BYTE j[dhprivkeyver3.bitlenJ/8]; 
            // Where J is (P-1)/Q
BYTE y[dhprivkeyver3.bitlenP/8]; 
            // Where Y is (G^X) mod P
BYTE x[dhprivkeyver3.bitlenX/8]; 
            // Where X is the private exponent
```



Esse formato de [*blob*](../secgloss/b-gly.md) é exportado quando o \_ sinalizador VER3 de blob cript \_ é usado com [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Como a versão está no BLOB, não é necessário especificar um sinalizador ao usar esse BLOB com [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

A tabela a seguir descreve cada componente do [*blob de chave*](../secgloss/k-gly.md).



| Campo         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Uma estrutura [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Uma estrutura [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) . O membro **mágico** deve ser definido como 0x34484400 para chaves privadas. Observe que o valor hexadecimal é apenas uma codificação [*ASCII*](../secgloss/a-gly.md) de "dh4".                                                                                                                                                                                                                                                                                            |
| P             | O valor P está localizado diretamente após a [**estrutura DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) e deve ser sempre o comprimento em bytes do campo **DHPRIVKEY \_ VER3** **bitlenP** (tamanho de bit P) dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                            |
| Q             | O valor Q está localizado diretamente após o valor P e deve ser sempre o comprimento em bytes do campo [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenQ** dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ). Se o valor de bitlenQ for 0, o valor estará ausente do BLOB.                                                                                                                                                                                                  |
| G             | O valor G está localizado diretamente após o valor Q e deve ser sempre o comprimento em bytes do campo [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (tamanho de bit p) dividido por oito. Se o comprimento dos dados for um ou mais bytes menores do que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado (o formato [*little-endian*](../secgloss/l-gly.md) ).                                                                 |
| J             | O valor J está localizado diretamente após o valor G e deve ser sempre o comprimento em bytes do campo [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenJ** dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ). Se o valor de bitlenJ for 0, o valor estará ausente do BLOB.                                                                                                                                                                                                  |
| S             | O valor Y, (G ^ X) mod P, está localizado diretamente após o valor J e deve ser sempre o comprimento em bytes do campo [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (tamanho de bit P) dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado ([*little-endian*](../secgloss/l-gly.md) ). |
| X             | O valor X é um inteiro grande aleatório, de modo que a parte pública do par de chaves DH, Y, seja igual a: Y = (G ^ X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave. A chave será criptografada se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão. Tudo menos a parte [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada. Observe que os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o [*blob de chave privada*](../secgloss/p-gly.md). O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.

> [!Note]  
> É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

 

 
