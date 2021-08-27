---
description: Descreve o formato de um BLOB de chave privada Diffie-Hellman versão 3.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: Diffie-Hellman blobs de chaves privadas da versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adeb61f7f64d7362e832ea395a125f9f25de9a5ac2ce82325645fd19745bb4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100826"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>Diffie-Hellman blobs de chaves privadas da versão 3

Quando um [*BLOB*](../secgloss/p-gly.md) Diffie-Hellman chave privada da versão 3 é exportado, ele está em um formato da seguinte forma:


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



Esse [*formato BLOB*](../secgloss/b-gly.md) é exportado quando o sinalizador CRYPT \_ BLOB \_ VER3 é usado com [**CryptExportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) Como a versão está no BLOB, não é necessário especificar um sinalizador ao usar esse BLOB com [**CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)

A tabela a seguir descreve cada componente do [*BLOB de chaves.*](../secgloss/k-gly.md)



| Campo         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Uma [**estrutura BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Uma [**estrutura DHPRIVKEY \_ VER3.**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) O **membro** mágico deve ser definido como 0x34484400 chaves privadas. Observe que o valor hexadecimal é apenas uma codificação [*ASCII*](../secgloss/a-gly.md) de "DH4".                                                                                                                                                                                                                                                                                            |
| P             | O valor P está localizado diretamente após a estrutura [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) e sempre deve ser o comprimento em bytes do campo **bitlenP** **DHPRIVKEY \_ VER3** (comprimento de bit de P) dividido por oito ([*formato little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                            |
| Q             | O valor de Q está localizado diretamente após o valor P e sempre deve ser o comprimento em bytes do campo **bitlenQ** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) dividido por oito ([*formato little-endian).*](../secgloss/l-gly.md) Se o valor de bitlenQ for 0, o valor será ausente do BLOB.                                                                                                                                                                                                  |
| G             | O valor G está localizado diretamente após o valor Q e sempre deve ser o comprimento em bytes do campo **bitlenP** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (comprimento de bit de P) dividido por oito. Se o comprimento dos dados for um ou mais bytes menor do que P dividido por 8, os dados deverão ser alojados com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado [*(formato little-endian).*](../secgloss/l-gly.md)                                                                 |
| J             | O valor J está localizado diretamente após o valor de G e sempre deve ser o comprimento em bytes do campo **bitlenJ** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) dividido por oito ([*formato little-endian).*](../secgloss/l-gly.md) Se o valor de bitlenJ for 0, o valor será ausente do BLOB.                                                                                                                                                                                                  |
| Y             | O valor Y, (G^X) mod P, está localizado diretamente após o valor J e sempre deve ser o comprimento em bytes do campo **bitlenP** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (comprimento de bit de P) dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G^X) mod P for um ou mais bytes menor do que P dividido por 8, os dados deverão ser alojados com os bytes necessários (de zero valor) para tornar os dados o comprimento desejado [*(formato little-endian).*](../secgloss/l-gly.md) |
| X             | O valor X é um inteiro grande aleatório, de modo que a parte pública do par de chaves DH, Y, é igual a: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deve criptografar a chave. A chave será criptografada se o *parâmetro hExpKey* contiver um alçado válido para uma chave de sessão. Tudo, menos [**a parte BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do BLOB, é criptografado. Observe que os parâmetros de chave de criptografia e algoritmo de criptografia não são armazenados junto com o [*BLOB de chave privada.*](../secgloss/p-gly.md) O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey,* a chave privada será exportada sem criptografia.

> [!Note]  
> É perigoso exportar chaves privadas sem criptografia porque elas ficam vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

 

 
