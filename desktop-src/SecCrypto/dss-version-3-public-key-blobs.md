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
# <a name="dss-version-3-public-key-blobs"></a><span data-ttu-id="f5552-103">BLOBs de chave pública do DSS versão 3</span><span class="sxs-lookup"><span data-stu-id="f5552-103">DSS Version 3 Public Key BLOBs</span></span>

<span data-ttu-id="f5552-104">Os [*blobs de chave pública*](../secgloss/p-gly.md) do DSS versão 3 do tipo PUBLICKEYBLOB são usados para exportar e importar informações sobre uma chave pública DH.</span><span class="sxs-lookup"><span data-stu-id="f5552-104">DSS version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) of type PUBLICKEYBLOB are used to export and import information about a DH public key.</span></span> <span data-ttu-id="f5552-105">Eles têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="f5552-105">They have the following format:</span></span>


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



<span data-ttu-id="f5552-106">Esse formato de [*blob*](../secgloss/b-gly.md) é exportado quando o \_ sinalizador VER3 de blob cript \_ é usado com [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="f5552-106">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="f5552-107">Como a versão está no BLOB, não é necessário especificar um sinalizador ao usar esse BLOB com [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="f5552-107">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="f5552-108">Além disso, esse formato de BLOB é usado com a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) quando o valor *dwParam* de KP \_ pub \_ params é usado para definir parâmetros de chave em uma chave DSS.</span><span class="sxs-lookup"><span data-stu-id="f5552-108">In addition, this BLOB format is used with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function when the *dwParam* value KP\_PUB\_PARAMS is used to set key parameters on a DSS key.</span></span> <span data-ttu-id="f5552-109">Isso é feito quando o \_ sinalizador cript PREGEN é usado para gerar a chave.</span><span class="sxs-lookup"><span data-stu-id="f5552-109">This is done when the CRYPT\_PREGEN flag has been used to generate the key.</span></span> <span data-ttu-id="f5552-110">Quando usado nessa situação, o valor y é ignorado e, portanto, não deve ser incluído no BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5552-110">When used in this situation, the y value is ignored and therefore should not be included in the BLOB.</span></span>

<span data-ttu-id="f5552-111">A tabela a seguir descreve cada componente do BLOB de chave.</span><span class="sxs-lookup"><span data-stu-id="f5552-111">The following table describes each component of the key BLOB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5552-112">Campo</span><span class="sxs-lookup"><span data-stu-id="f5552-112">Field</span></span></th>
<th><span data-ttu-id="f5552-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5552-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5552-114">Blobheader</span><span class="sxs-lookup"><span data-stu-id="f5552-114">Blobheader</span></span></td>
<td><span data-ttu-id="f5552-115">Uma estrutura <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f5552-115">A <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> structure.</span></span> <span data-ttu-id="f5552-116">O membro <strong>bType</strong> deve ter um valor de PublicKeyBlob.</span><span class="sxs-lookup"><span data-stu-id="f5552-116">The <strong>bType</strong> member must have a value of PUBLICKEYBLOB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5552-117">Dsspubkeyver3</span><span class="sxs-lookup"><span data-stu-id="f5552-117">Dsspubkeyver3</span></span></td>
<td><span data-ttu-id="f5552-118">Uma estrutura de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f5552-118">A <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure.</span></span> <span data-ttu-id="f5552-119">O membro <strong>mágico</strong> deve ser definido como &quot; DSS3 &quot; (0x33535344) para chaves públicas.</span><span class="sxs-lookup"><span data-stu-id="f5552-119">The <strong>magic</strong> member should be set to &quot;DSS3&quot; (0x33535344) for public keys.</span></span> <span data-ttu-id="f5552-120">Observe que o valor hexadecimal é apenas uma codificação <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> de &quot; DSS3.&quot;</span><span class="sxs-lookup"><span data-stu-id="f5552-120">Notice that the hexadecimal value is just an <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> encoding of &quot;DSS3.&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5552-121">P</span><span class="sxs-lookup"><span data-stu-id="f5552-121">P</span></span></td>
<td><span data-ttu-id="f5552-122">O valor P está localizado diretamente após a estrutura de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> e deve ser sempre o comprimento, em bytes, do campo DSSPUBKEY_VER3 <strong>bitlenP</strong> (tamanho de bit P) dividido por oito (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="f5552-122">The P value is located directly after the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure, and should always be the length, in bytes, of the DSSPUBKEY_VER3 <strong>bitlenP</strong> field (bit length of P) divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5552-123">Q</span><span class="sxs-lookup"><span data-stu-id="f5552-123">Q</span></span></td>
<td><span data-ttu-id="f5552-124">O valor Q está localizado diretamente após o valor P e deve ser sempre o comprimento em bytes do membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> dividido por oito (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="f5552-124">The Q value is located directly after the P value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5552-125">G</span><span class="sxs-lookup"><span data-stu-id="f5552-125">G</span></span></td>
<td><span data-ttu-id="f5552-126">O valor G está localizado diretamente após o valor Q e deve ser sempre o comprimento, em bytes, do membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (comprimento de bit p) dividido por oito.</span><span class="sxs-lookup"><span data-stu-id="f5552-126">The G value is located directly after the Q value and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="f5552-127">Se o comprimento dos dados for um ou mais bytes menores do que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado (o formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="f5552-127">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5552-128">J</span><span class="sxs-lookup"><span data-stu-id="f5552-128">J</span></span></td>
<td><span data-ttu-id="f5552-129">O valor J está localizado diretamente após o valor G e deve ser sempre o comprimento em bytes do membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> dividido por oito (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="f5552-129">The J value is located directly after the G value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span> <span data-ttu-id="f5552-130">Se o valor de bitlenQ for 0, o valor estará ausente do BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5552-130">If the bitlenQ value is 0, then the value is absent from the BLOB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5552-131">S</span><span class="sxs-lookup"><span data-stu-id="f5552-131">Y</span></span></td>
<td><span data-ttu-id="f5552-132">O valor Y, (G ^ X) mod P, está localizado diretamente após o valor J e deve ser sempre o comprimento, em bytes, do membro de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (comprimento de bit P) dividido por oito.</span><span class="sxs-lookup"><span data-stu-id="f5552-132">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="f5552-133">Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por 8, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="f5552-133">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f5552-134">Quando essa estrutura é usada com <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> com o valor de <em>dwParam</em> KP_PUB_PARAMS, esse valor não é incluído no BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5552-134">When this structure is used with <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> with the <em>dwParam</em> value KP_PUB_PARAMS, then this value is not included in the BLOB.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="f5552-135">Os BLOBs de chave pública não são criptografados, mas contêm chaves públicas em formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="f5552-135">Public key BLOBs are not encrypted, but contain public keys in plaintext form.</span></span>

 

 

 
