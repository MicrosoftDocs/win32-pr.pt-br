---
description: Descreve o formato de uma chave privada exportada do DSS versão 3.
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: BLOBs de chave privada do DSS versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6434e411ba3268901176a5c9739ceecfa79689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169485"
---
# <a name="dss-version-3-private-key-blobs"></a>BLOBs de chave privada do DSS versão 3

Quando uma [*chave privada*](../secgloss/p-gly.md) de [*DSS*](../secgloss/d-gly.md) de versão 3 é exportada, ela está em um formato da seguinte maneira:


```C++
BLOBHEADER        blobheader; 
DSSPRIVKEY_VER3   dssprivkeyver3;
BYTE p[dssprivkeyver3.bitlenP/8]; 
                    // Where P is the prime modulus
BYTE q[dssprivkeyver3.bitlenQ/8]; 
                    // Where Q is a large factor of P-1
BYTE g[dssprivkeyver3.bitlenP/8]; 
                    // Where G is the generator parameter
BYTE j[dssprivkeyver3.bitlenJ/8]; 
                    // Where J is (P-1)/Q
BYTE y[dssprivkeyver3.bitlenP/8]; 
                    // Where Y is (G^X) mod P
BYTE x[dssprivkeyver3.bitlenX/8]; 
                    // Where X is the private exponent
```



Esse formato de [*blob*](../secgloss/b-gly.md) é exportado quando o \_ sinalizador VER3 de blob cript \_ é usado com [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Como a versão está no BLOB, não é necessário especificar um sinalizador ao usar esse BLOB com [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

A tabela a seguir descreve cada componente do [*blob de chave*](../secgloss/k-gly.md).



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | Uma estrutura [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) . O membro **bType** deve ter um valor de PublicKeyBlob.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | Uma estrutura **DSSPRIVKEY \_ VER3** . O membro **mágico** deve ser definido como "DSS4" (0x34535344) para chaves privadas. Observe que o valor hexadecimal é apenas uma codificação [*ASCII*](../secgloss/a-gly.md) de "DSS4".<br/>                                                                                                                                                                                                                                                                     |
| P              | O valor P está localizado diretamente após a estrutura **DSSPRIVKEY \_ VER3** e deve ser sempre o comprimento, em bytes, do campo **DSSPRIVKEY \_ VER3 BitlenP** (comprimento de bit P) dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                           |
| Q              | O valor Q está localizado diretamente após o valor P e deve sempre ser o comprimento, em bytes, do campo **DSSPRIVKEY \_ VER3 bitlenQ** dividido por oito ([*little-endian*](../secgloss/l-gly.md) Format).                                                                                                                                                                                                                                                                     |
| G              | O valor G está localizado diretamente após o valor Q e deve ser sempre o comprimento, em bytes, do campo **DSSPRIVKEY \_ VER3 bitlenP** (tamanho de bit P) dividido por oito. Se o comprimento dos dados for um ou mais bytes menores do que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado (o formato [*little-endian*](../secgloss/l-gly.md) ).                                                                 |
| J              | O valor J está localizado diretamente após o valor G e deve sempre ser o comprimento, em bytes, do campo **DSSPRIVKEY \_ VER3 bitlenJ** dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ). Se o valor de bitlenJ for 0, o valor estará ausente do BLOB.                                                                                                                                                                                                   |
| S              | O valor Y, (G ^ X) mod P, está localizado diretamente após o valor J e deve ser sempre o comprimento, em bytes, do campo **DSSPRIVKEY \_ VER3 bitlenP** (tamanho de bit P) dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado ([*little-endian*](../secgloss/l-gly.md) ). |
| X              | O valor X é um inteiro grande aleatório, de modo que a parte pública do par de chaves DH, Y, seja igual a: Y = (G ^ X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave. A chave será criptografada se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão. Tudo menos a parte [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada. Observe que os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o [*blob de chave privada*](../secgloss/p-gly.md). O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.

> [!IMPORTANT]
> É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

 

 
