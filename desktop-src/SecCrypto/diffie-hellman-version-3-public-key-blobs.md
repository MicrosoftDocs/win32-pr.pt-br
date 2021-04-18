---
description: Os BLOBs de chave pública Diffie-Hellman versão 3 (tipo PUBLICKEYBLOB) são usados para exportar e importar informações sobre uma chave pública DH.
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: BLOBs de chave pública do Diffie-Hellman versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7228e4b4a786dc0eb25d1ba199b5c20923dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756859"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>BLOBs de chave pública do Diffie-Hellman versão 3

Os [*blobs de chave pública*](../secgloss/p-gly.md) Diffie-Hellman versão 3 (tipo PublicKeyBlob) são usados para exportar e importar informações sobre uma chave pública DH. Eles têm o seguinte formato:


```C++
BLOBHEADER blobheader; 
                 // As explained under "Data Structures"
DHPUBKEY_VER3 dhpubkeyver3;
BYTE p[dhpubkeyver3.bitlenP/8]; 
                 // Where P is the prime modulus
BYTE q[dhpubkeyver3.bitlenQ/8]; 
                 // Where Q is a large factor of P-1
BYTE g[dhpubkeyver3.bitlenP/8]; 
                 // Where G is the generator parameter
BYTE j[dhpubkeyver3.bitlenJ/8]; 
                 // Where J is (P-1)/Q
BYTE y[dhpubkeyver3.bitlenP/8]; 
                 // Where Y is (G^X) mod P
```



Esse formato de BLOB é exportado quando o \_ sinalizador VER3 de blob cript \_ é usado com [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Como a versão está no BLOB, não é necessário especificar um sinalizador ao usar esse [*blob*](../secgloss/b-gly.md) com [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Além disso, esse formato de BLOB é usado com a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) quando o valor *dwParam* de KP \_ pub \_ params é usado para definir parâmetros de chave em uma chave DH. Isso é feito quando o \_ sinalizador cript PREGEN é usado para gerar a chave. Quando usado nessa situação, o valor y é ignorado e, portanto, não deve ser incluído no BLOB.

A tabela a seguir descreve cada componente do BLOB de chave.



| Campo        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Uma estrutura [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) . O membro **bType** deve ter um valor de PublicKeyBlob.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Uma estrutura [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) . O membro **mágico** deve ser definido como 0x33484400 para chaves públicas. Observe que o valor hexadecimal é apenas uma codificação [*ASCII*](../secgloss/a-gly.md) de "DH3".                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | O valor P está localizado diretamente após a [**estrutura DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) e deve ser sempre o comprimento, em bytes, do campo **DHPUBKEY \_ VER3** **bitlenP** (comprimento de bit P) dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | O valor Q está localizado diretamente após o valor P e deve ser sempre o comprimento em bytes do campo [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenQ** dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ). Se o valor de bitlenQ for 0, o valor estará ausente do BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | O valor G está localizado diretamente após o valor Q e deve ser sempre o comprimento, em bytes, do campo [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (tamanho de bit P) dividido por oito. Se o comprimento dos dados for um ou mais bytes menores do que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado (o formato [*little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                              |
| J            | O valor J está localizado diretamente após o valor G e deve ser sempre o comprimento em bytes do campo [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenJ** dividido por oito (formato [*little-endian*](../secgloss/l-gly.md) ). Se o valor de bitlenQ for 0, o valor estará ausente do BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| S            | O valor Y, (G ^ X) mod P, está localizado diretamente após o valor J e deve ser sempre o comprimento em bytes do campo [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (tamanho de bit P) dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado ([*little-endian*](../secgloss/l-gly.md) ). Quando essa estrutura é usada com [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) com o valor *dwParam* de KP \_ pub \_ params, esse valor não é incluído no BLOB. |



 

> [!Note]  
> Os BLOBs de chave pública não são criptografados, mas contêm chaves públicas em formato de texto sem formatação.

 

 

 
