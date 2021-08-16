---
description: Descreve o formato de uma chave privada do DSS versão 3 exportada.
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: BLOBs de Chaves Privadas do DSS versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6706f8cbfccb8c836efefb99a30086dc459619c8477b773a557f503ebbb2243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767251"
---
# <a name="dss-version-3-private-key-blobs"></a>BLOBs de Chaves Privadas do DSS versão 3

Quando uma chave privada [*DSS*](../secgloss/d-gly.md) [](../secgloss/p-gly.md) versão 3 é exportada, ela está em um formato da seguinte forma:


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



Esse [*formato BLOB*](../secgloss/b-gly.md) é exportado quando o sinalizador CRYPT \_ BLOB \_ VER3 é usado com [**CryptExportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) Como a versão está no BLOB, não é necessário especificar um sinalizador ao usar esse BLOB com [**CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)

A tabela a seguir descreve cada componente do [*BLOB de chaves.*](../secgloss/k-gly.md)



| Campo          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | Uma [**estrutura BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) O **membro bType** deve ter um valor de PUBLICKEYBLOB.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | Uma **estrutura DSSPRIVKEY \_ VER3.** O **membro** mágico deve ser definido como "DSS4" (0x34535344) para chaves privadas. Observe que o valor hexadecimal é apenas uma codificação [*ASCII*](../secgloss/a-gly.md) de "DSS4".<br/>                                                                                                                                                                                                                                                                     |
| P              | O valor P está localizado diretamente após a estrutura **DSSPRIVKEY \_ VER3** e sempre deve ser o comprimento, em bytes, do campo **\_ bitlenP DSSPRIVKEY VER3** (comprimento de bit de P) dividido por oito ([*formato little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                           |
| Q              | O valor Q está localizado diretamente após o valor P e sempre deve ser o comprimento, em bytes, do campo **\_ bitlenQ DSSPRIVKEY VER3** dividido por oito ([*formato little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                                                                     |
| G              | O valor G está localizado diretamente após o valor Q e sempre deve ser o comprimento, em bytes, do campo **\_ bitlenP DSSPRIVKEY VER3** (comprimento de bit de P) dividido por oito. Se o comprimento dos dados for um ou mais bytes menor do que P dividido por 8, os dados deverão ser alojados com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado [*(formato little-endian).*](../secgloss/l-gly.md)                                                                 |
| J              | O valor J está localizado diretamente após o valor de G e sempre deve ser o comprimento, em bytes, do campo **\_ bitlenJ DSSPRIVKEY VER3** dividido por oito ([*formato little-endian).*](../secgloss/l-gly.md) Se o valor de bitlenJ for 0, o valor será ausente do BLOB.                                                                                                                                                                                                   |
| Y              | O valor Y, (G^X) mod P, está localizado diretamente após o valor J e sempre deve ser o comprimento, em bytes, do campo **\_ bitlenP DSSPRIVKEY VER3** (comprimento de bit de P) dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G^X) mod P for um ou mais bytes menor do que P dividido por 8, os dados deverão ser alojados com os bytes necessários (de zero valor) para tornar os dados o comprimento desejado [*(formato little-endian).*](../secgloss/l-gly.md) |
| X              | O valor X é um inteiro grande aleatório, de modo que a parte pública do par de chaves DH, Y, é igual a: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deve criptografar a chave. A chave será criptografada se o *parâmetro hExpKey* contiver um alçado válido para uma chave de sessão. Tudo, menos [**a parte BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do BLOB, é criptografado. Observe que os parâmetros de chave de criptografia e algoritmo de criptografia não são armazenados junto com o [*BLOB de chave privada.*](../secgloss/p-gly.md) O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey,* a chave privada será exportada sem criptografia.

> [!IMPORTANT]
> É perigoso exportar chaves privadas sem criptografia porque elas ficam vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

 

 
