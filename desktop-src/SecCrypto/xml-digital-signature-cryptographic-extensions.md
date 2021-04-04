---
description: O CryptXML permite que os desenvolvedores estendam algoritmos de criptografia com suporte nativo registrando uma DLL de extensão de criptografia de todo o sistema.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Extensões criptográficas de assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103837544"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Extensões criptográficas de assinatura digital XML

O CryptXML permite que os desenvolvedores estendam algoritmos de criptografia com suporte nativo registrando uma DLL de extensão de criptografia de todo o sistema. As DLLs de extensão estendem os algoritmos com suporte pelos elementos XML **SignatureMethod** e **DigestMethod** . DLLs de extensão podem dar suporte a algoritmos que codificam parâmetros adicionais na assinatura digital XML.

Todas as DLLs de extensões devem oferecer suporte à função [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , que retorna um ponteiro para uma estrutura de [**\_ \_ \_ interface criptográfica XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) . Essa estrutura fornece ponteiros de função para implementar funções de extensão criptográfica. As funções com suporte dependem do tipo de algoritmo criptográfico com suporte e se o algoritmo deve codificar parâmetros na assinatura digital XML.

As funções de extensões criptográficas incluem os seguintes ponteiros de função:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funções necessárias
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funções de método Digest
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funções de método de assinatura
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Para algoritmos com parâmetros codificados padrão
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

As DLLs de extensão criptográfica são registradas em todo o sistema. São necessários privilégios de administrador para registrar uma DLL de extensão criptográfica.

Todas as extensões criptográficas CryptXML são registradas pelo valor de URI definido no campo **SignatureMethod** ou atributo de algoritmo do elemento **DigestMethod** .

Os caminhos de registro para as DLLs de extensão são os seguintes:

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32 bits
</dt> <dd>

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64 bits
</dt> <dd>

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

**HKEY \_ \_Computador local** \\ **software** \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> </dl>

Cada chave contém as configurações a seguir.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Dados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DLL<br/></td>
<td>Cadeia de caracteres expansível<br/></td>
<td>Obrigatórios.<br/>O caminho absoluto para a DLL do provedor criptográfico XML.
<blockquote>
<p><b>Observação: </b> Recomendamos que as DLLs de extensão criptográficas estejam localizadas em diretórios que só possam ser gravados por aplicativos com privilégio administrativo.</p>
<p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> é usado para carregar a DLL de extensão criptográfica.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Nome<br/></td>
<td><strong>Cadeia de caracteres</strong></td>
<td>Opcional.<br/> O nome de exibição associado a esse URI.<br/></td>
</tr>
<tr class="odd">
<td>GroupId<br/></td>
<td><strong>DWORD</strong></td>
<td>Obrigatórios.<br/> O identificador de grupo associado a este algoritmo criptográfico. Os valores possíveis incluem o seguinte:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1<br/><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2<br/></td>
</tr>
<tr class="even">
<td>CNGAlgid<br/></td>
<td><strong>Cadeia de caracteres</strong></td>
<td>Obrigatórios.<br/> O nome do algoritmo CNG a ser passado para as funções BCrypt ou NCrypt.<br/></td>
</tr>
<tr class="odd">
<td>CNGExtraAlgid<br/></td>
<td><strong>Cadeia de caracteres</strong></td>
<td>Opcional.<br/> Uma cadeia de caracteres de algoritmo extra, diferente da cadeia de caracteres no membro CNGAlgid, que pode ser passada para as funções CNG.<br/> Para os algoritmos de assinatura (CRYPT_XML_GROUP_ID_SIGN), esse membro é a cadeia de caracteres de algoritmo de chave pública a ser passada para as funções CNG.<br/> Para os outros valores de GroupId, defina o membro <strong>pwszCNGExtraAlgid</strong> como a cadeia de caracteres vazia, L &quot; &quot; . <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[Algoritmos criptográficos de assinatura digital XML](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
