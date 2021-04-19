---
description: Define os códigos de erro retornados pelo CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Enumeração de CAPICOM_ERROR_CODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756561"
---
# <a name="capicom_error_code-enumeration"></a>Enumeração de código de \_ erro CApicom \_

O tipo de enumeração de **\_ \_ código de erro capicod** define códigos de erro que são retornados pelo CAPICOM.

> [!Note]  
> Visual Basic Scripting Edition erros retornam um valor **Err. Number** maior que zero. Para esses erros, os valores **Err. Description** fornecem informações sobre a causa do erro. Além dos erros de Visual Basic Scripting Edition, os erros CAPICOM retornam os códigos definidos pelo **\_ \_ código de erro CAPICOM**.

 

## <a name="members"></a>Membros



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro</th>
<th>DESCRIÇÃO</th>
<th>Valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></td>
<td>Um tipo de codificação inválido foi usado.<br/> A lista a seguir mostra os tipos de codificação válidos:
<ul>
<li>CAPICOM_ENCODE_ANY</li>
<li>CAPICOM_ENCODE_BASE64</li>
<li>CAPICOM_ENCODE_BINARY</li>
</ul>
<br/></td>
<td>0x80880100</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EKU_INVALID_OID</strong></td>
<td>A propriedade <a href="eku-oid.md"><strong>OID</strong></a> do objeto <a href="eku.md"><strong>EKU</strong></a> não pode ser definida porque a propriedade <a href="eku-name.md"><strong>Name</strong></a> não está definida como CAPICOM_EKU_OTHER.<br/> Defina a propriedade <a href="eku-name.md"><strong>Name</strong></a> como CAPICOM_EKU_OTHER antes de definir a propriedade <a href="eku-oid.md"><strong>OID</strong></a> .<br/></td>
<td>0x80880200</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></td>
<td>A propriedade <a href="eku-oid.md"><strong>OID</strong></a> do objeto <a href="eku.md"><strong>EKU</strong></a> não foi inicializada. <br/> Defina a propriedade <a href="eku-name.md"><strong>Name</strong></a> para qualquer coisa diferente de CAPICOM_EKU_OTHER, ou defina a propriedade <strong>Name</strong> como CAPICOM_EKU_OTHER e a propriedade <a href="eku-oid.md"><strong>OID</strong></a> como um valor.<br/></td>
<td>0x80880201</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></td>
<td>O objeto de <a href="certificate.md"><strong>certificado</strong></a> não foi inicializado.<br/> Normalmente, esse código de erro é retornado quando um objeto de <a href="certificate.md"><strong>certificado</strong></a> é instanciado, mas não associado a um certificado digital. Para associar o objeto a um certificado digital, atribua-o a um objeto de <strong>certificado</strong> existente ou chame o método de <a href="certificate-import.md"><strong>importação</strong></a> .<br/></td>
<td>0x80880210</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></td>
<td>O objeto de <a href="certificate.md"><strong>certificado</strong></a> não tem uma chave privada associada.<br/> Esse código de erro é retornado quando é feita uma tentativa de assinar dados usando a chave privada do signatário, mas o objeto de <a href="certificate.md"><strong>certificado</strong></a> associado ao objeto de <a href="signer.md"><strong>signatário</strong></a> não pode ser usado para a operação de assinatura.<br/></td>
<td>0x80880211</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></td>
<td>O objeto de <a href="chain.md"><strong>cadeia</strong></a> não foi inicializado. <br/> Para inicializar o objeto <a href="chain.md"><strong>Chain</strong></a> , chame o método <a href="chain-build.md"><strong>Build</strong></a> .<br/></td>
<td>0x80880220</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_NOT_OPENED</strong></td>
<td>O objeto de <a href="store.md"><strong>repositório</strong></a> não foi inicializado. <br/> Para inicializar o objeto de <a href="store.md"><strong>armazenamento</strong></a> , chame o método <a href="store-open.md"><strong>Open</strong></a> .<br/></td>
<td>0x80880230</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_EMPTY</strong></td>
<td>O objeto de <a href="store.md"><strong>repositório</strong></a> não contém nenhum objeto de <a href="certificate.md"><strong>certificado</strong></a> .<br/></td>
<td>0x80880231</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></td>
<td>O parâmetro <em>OpenMode</em> do método <a href="store-open.md"><strong>Store. Open</strong></a> não contém um valor válido de CAPICOM_STORE_OPEN_MODE.<br/> A lista a seguir mostra os valores válidos de CAPICOM_STORE_OPEN_MODE:
<ul>
<li>CAPICOM_STORE_OPEN_READ_ONLY</li>
<li>CAPICOM_STORE_OPEN_READ_WRITE</li>
<li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li>
<li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li>
<li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li>
</ul>
<br/></td>
<td>0x80880232</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></td>
<td>O valor de <em>SaveAs</em> passado para o método <a href="store-export.md"><strong>Export</strong></a> do objeto <a href="store.md"><strong>Store</strong></a> não era válido. <br/> A lista a seguir mostra os valores válidos de <em>SaveAs</em> :
<ul>
<li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li>
<li>CAPICOM_STORE_SAVE_AS_PKCS7</li>
</ul>
<br/></td>
<td>0x80880233</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></td>
<td>A propriedade <a href="attribute-name.md"><strong>Name</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não foi inicializada. <br/> Defina a propriedade <a href="attribute-name.md"><strong>Name</strong></a> .<br/></td>
<td>0x80880240</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></td>
<td>A propriedade <a href="attribute-value.md"><strong>Value</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não foi inicializada. <br/> Defina a propriedade <a href="attribute-value.md"><strong>valor</strong></a> .<br/></td>
<td>0x80880241</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></td>
<td>A propriedade <a href="attribute-name.md"><strong>Name</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não é válida. <br/> A lista a seguir mostra os nomes de atributo válidos:
<ul>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li>
</ul>
<br/></td>
<td>0x80880242</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></td>
<td>A propriedade <a href="attribute-value.md"><strong>Value</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não é válida porque o tipo de dados não corresponde ao tipo de dados indicado pela propriedade <strong>Name</strong> . <br/> Por exemplo, se a propriedade <a href="attribute-value.md"><strong>Name</strong></a> for definida como CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, o tipo de dados deverá ser <strong>Date</strong>.<br/></td>
<td>0x80880243</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></td>
<td>O objeto de <a href="signer.md"><strong>signatário</strong></a> não foi inicializado. <br/> Para inicializar o objeto de <a href="signer.md"><strong>signatário</strong></a> , defina a propriedade de <a href="signer-certificate.md"><strong>certificado</strong></a> .<br/></td>
<td>0x80880250</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></td>
<td>Não é possível encontrar o signatário no objeto <a href="signeddata.md"><strong>SignedData</strong></a> . <br/> Normalmente, isso não acontece com um objeto <a href="signeddata.md"><strong>SignedData</strong></a> que foi criado pelo CAPICOM; no entanto, se o objeto <strong>SignedData</strong> foi criado por um produto de terceiros, o certificado do assinante pode não ser incluído na estrutura de #7 PKCS.<br/></td>
<td>0x80880251</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></td>
<td>Não é possível encontrar um objeto de <a href="chain.md"><strong>cadeia</strong></a> no objeto de <a href="signer.md"><strong>signatário</strong></a> .<br/></td>
<td>0x80880252//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></td>
<td>É feita uma tentativa de usar o Assinante de uma forma que não seja válida.<br/></td>
<td>0x80880253 //v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></td>
<td>O objeto <a href="signeddata.md"><strong>SignedData</strong></a> não foi inicializado. <br/> Para inicializar o objeto <a href="signeddata.md"><strong>SignedData</strong></a> , defina a propriedade <a href="signeddata-content.md"><strong>Content</strong></a> ou chame o método <a href="signeddata-verify.md"><strong>Verify</strong></a> .<br/></td>
<td>0x80880260</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></td>
<td>O objeto <a href="signeddata.md"><strong>SignedData</strong></a> contém um tipo que não é válido. <br/> Normalmente, isso acontece quando é feita uma tentativa de verificar uma mensagem envelopada com um objeto <a href="signeddata.md"><strong>SignedData</strong></a> ou vice-versa.<br/></td>
<td>0x80880261</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></td>
<td>O objeto <a href="signeddata.md"><strong>SignedData</strong></a> não foi assinado. <br/> Para assinar o objeto <a href="signeddata.md"><strong>SignedData</strong></a> , chame o método <a href="signeddata-sign.md"><strong>Sign</strong></a> .<br/></td>
<td>0x80880262</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_ALGORITHM</strong></td>
<td>O valor do algoritmo para a propriedade <a href="algorithm-name.md"><strong>Name</strong></a> do objeto de <a href="algorithm.md"><strong>algoritmo</strong></a> não é válido. <br/> A lista a seguir mostra os valores de algoritmo válidos para a propriedade <a href="algorithm-name.md"><strong>Name</strong></a> :
<ul>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li>
</ul>
<br/></td>
<td>0x80880270</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></td>
<td>O valor de comprimento da chave para a propriedade <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> do objeto de <a href="algorithm.md"><strong>algoritmo</strong></a> não é válido. <br/> A lista a seguir mostra os valores de comprimento de chave válidos para a propriedade <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> :
<ul>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li>
</ul>
<br/></td>
<td>0x80880271</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></td>
<td>O objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> não foi inicializado. <br/> Para inicializar o objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , defina a propriedade <a href="envelopeddata-content.md"><strong>Content</strong></a> ou chame o método <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .<br/></td>
<td>0x80880280</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></td>
<td>O objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contém um tipo que não é válido. <br/> Normalmente, isso acontece quando é feita uma tentativa de verificar uma mensagem assinada com um objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> ou vice-versa.<br/></td>
<td>0x80880281</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></td>
<td>Não há nenhum destinatário especificado no objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> quando o método <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> de um objeto <strong>EnvelopedData</strong> é chamado. <br/> Para adicionar um destinatário, chame o método <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .<br/></td>
<td>0x80880282</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></td>
<td>O destinatário não pode ser encontrado no objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> . <br/> Normalmente, isso não acontece com um objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> que foi criado pelo CAPICOM; no entanto, se o objeto <strong>EnvelopedData</strong> foi criado por um produto de terceiros, o certificado do destinatário pode não estar incluído na estrutura de #7 PKCS.<br/></td>
<td>0x80880283</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></td>
<td>O objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> não foi inicializado. <br/> Para inicializar o objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , defina a propriedade <a href="encrypteddata-content.md"><strong>Content</strong></a> ou chame o método <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> .<br/></td>
<td>0x80880290</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></td>
<td>O objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> não é um tipo válido. <br/> Normalmente, isso significa que os dados estão corrompidos.<br/></td>
<td>0x80880291</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></td>
<td>O segredo de um objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> não foi inicializado. <br/> Para inicializar o segredo de um objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , chame o método <a href="encrypteddata-setsecret.md"><strong>setsecret</strong></a> .<br/></td>
<td>0x80880292</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></td>
<td>O objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> não foi inicializado.<br/></td>
<td>0x80880300//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></td>
<td>O objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> não pode ser exportado.<br/></td>
<td>0x80880301//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></td>
<td>O objeto <a href="encodeddata.md"><strong>EncodedData</strong></a> não foi inicializado.<br/></td>
<td>0x80880320//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></td>
<td>O objeto de <a href="extension.md"><strong>extensão</strong></a> não foi inicializado.<br/></td>
<td>0x80880330//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></td>
<td>A propriedade <a href="extendedproperty-propid.md"><strong>Propid</strong></a> do objeto <a href="extendedproperty.md"><strong>Extended</strong></a> não foi inicializada.<br/></td>
<td>0x80880340//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></td>
<td>O parâmetro <em>FindType</em> do método <a href="certificates-find.md"><strong>Certificates. Find</strong></a> não é um valor da enumeração <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .<br/></td>
<td>0x80880350//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></td>
<td>A política predefinida especificada para a operação Localizar não é válida.<br/></td>
<td>0x80880351//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></td>
<td>O objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi inicializado.<br/></td>
<td>0x80880360//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></td>
<td>O objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi assinado.<br/> Para assinar o objeto <a href="signedcode.md"><strong>SignedCode</strong></a> , chame o método <a href="signedcode-sign.md"><strong>Sign</strong></a> .<br/></td>
<td>0x80880361//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></td>
<td>A propriedade <a href="signedcode-description.md"><strong>Description</strong></a> do objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi inicializada.<br/></td>
<td>0x80880362//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></td>
<td>A propriedade <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> do objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi inicializada.<br/></td>
<td>0x80880363//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></td>
<td>O parâmetro de <em>URL</em> do método <a href="signedcode-timestamp.md"><strong>SignedCode. Timestamp</strong></a> não é válido.<br/></td>
<td>0x80880364//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_HASH_NO_DATA</strong></td>
<td>O objeto <a href="hasheddata.md"><strong>HashedData</strong></a> não contém nenhum dado.<br/></td>
<td>0x80880370//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></td>
<td>O tipo de conversão não é válido.<br/></td>
<td>0x80880380//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_NOT_SUPPORTED</strong></td>
<td>A operação solicitada não tem suporte na plataforma atual. <br/></td>
<td>0x80880900</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_UI_DISABLED</strong></td>
<td>Ao assinar, a propriedade de <a href="signer-certificate.md"><strong>certificado</strong></a> do objeto de <a href="signer.md"><strong>signatário</strong></a> não foi definida, mas o prompt para o certificado de usuário foi desabilitado. <br/> Habilite o prompt definindo a propriedade <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> do objeto de <a href="settings.md"><strong>configurações</strong></a> ou defina a propriedade de <a href="signer-certificate.md"><strong>certificado</strong></a> do objeto de <a href="signer.md"><strong>signatário</strong></a> .<br/></td>
<td>0x80880901</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CANCELLED</strong></td>
<td>A operação foi cancelada pelo usuário. <br/> Isso acontece quando o usuário é solicitado a fornecer permissão para realizar uma determinada operação, como acessar a chave privada, e o usuário cancela a operação.<br/></td>
<td>0x80880902</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_NOT_ALLOWED</strong></td>
<td>A operação tentada não é permitida.<br/> Por exemplo, a alteração da propriedade <a href="extendedproperty-propid.md"><strong>Propid</strong></a> de um objeto <a href="extendedproperty.md"><strong>Extended</strong></a> não será permitida se o objeto estiver anexado a um certificado.<br/></td>
<td>0x80880903//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></td>
<td>O capicont ficou sem um recurso.<br/></td>
<td>0x80880904//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INTERNAL</strong></td>
<td>Ocorreu um erro interno. <br/> Contate o suporte técnico da Microsoft para obter assistência.<br/></td>
<td>0x80880911</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_UNKNOWN</strong></td>
<td>Ocorreu um erro desconhecido. <br/> Colete o máximo de informações possível e entre em contato com seu fornecedor.<br/></td>
<td>0x80880999</td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




