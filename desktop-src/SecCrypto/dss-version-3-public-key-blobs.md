---
description: Os BLOBs de chave pública do DSS versão 3 do tipo PUBLICKEYBLOB são usados para exportar e importar informações sobre uma chave pública DH.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: BLOBs de chave pública do DSS versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780473"
---
# <a name="dss-version-3-public-key-blobs"></a>BLOBs de chave pública do DSS versão 3

Os [*blobs de chave pública*](../secgloss/p-gly.md) do DSS versão 3 do tipo PUBLICKEYBLOB são usados para exportar e importar informações sobre uma chave pública DH. Eles têm o seguinte formato:


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



Esse formato de [*blob*](../secgloss/b-gly.md) é exportado quando o \_ sinalizador VER3 de blob cript \_ é usado com [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Como a versão está no BLOB, não é necessário especificar um sinalizador ao usar esse BLOB com [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Além disso, esse formato de BLOB é usado com a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) quando o valor *dwParam* de KP \_ pub \_ params é usado para definir parâmetros de chave em uma chave DSS. Isso é feito quando o \_ sinalizador cript PREGEN é usado para gerar a chave. Quando usado nessa situação, o valor y é ignorado e, portanto, não deve ser incluído no BLOB.

A tabela a seguir descreve cada componente do BLOB de chave.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blobheader</td>
<td>Uma estrutura <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> . O membro <strong>bType</strong> deve ter um valor de PublicKeyBlob.</td>
</tr>
<tr class="even">
<td>Dsspubkeyver3</td>
<td>Uma estrutura de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> . O membro <strong>mágico</strong> deve ser definido como &quot; DSS3 &quot; (0x33535344) para chaves públicas. Observe que o valor hexadecimal é apenas uma codificação <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> de &quot; DSS3.&quot;<br/></td>
</tr>
<tr class="odd">
<td>P</td>
<td>O valor P está localizado diretamente após a estrutura de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> e deve ser sempre o comprimento, em bytes, do campo DSSPUBKEY_VER3 <strong>bitlenP</strong> (tamanho de bit P) dividido por oito (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</td>
</tr>
<tr class="even">
<td>Q</td>
<td>O valor Q está localizado diretamente após o valor P e deve ser sempre o comprimento em bytes do membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> dividido por oito (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</td>
</tr>
<tr class="odd">
<td>G</td>
<td>O valor G está localizado diretamente após o valor Q e deve ser sempre o comprimento, em bytes, do membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (comprimento de bit p) dividido por oito. Se o comprimento dos dados for um ou mais bytes menores do que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado (o formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</td>
</tr>
<tr class="even">
<td>J</td>
<td>O valor J está localizado diretamente após o valor G e deve ser sempre o comprimento em bytes do membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> dividido por oito (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ). Se o valor de bitlenQ for 0, o valor estará ausente do BLOB.</td>
</tr>
<tr class="odd">
<td>S</td>
<td>O valor Y, (G ^ X) mod P, está localizado diretamente após o valor J e deve ser sempre o comprimento, em bytes, do membro de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (comprimento de bit P) dividido por oito. Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).
<blockquote>
[!Note]<br />
Quando essa estrutura é usada com <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> com o valor de <em>dwParam</em> KP_PUB_PARAMS, esse valor não é incluído no BLOB.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Os BLOBs de chave pública não são criptografados, mas contêm chaves públicas em formato de texto sem formatação.

 

 

 
