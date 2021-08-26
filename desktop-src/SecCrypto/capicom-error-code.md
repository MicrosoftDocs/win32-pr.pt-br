---
description: Define códigos de erro retornados pelo CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: CAPICOM_ERROR_CODE enumeração (Capicom.h)
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
ms.openlocfilehash: abdd2556ace3e3c3c82ccdeedc907d77f9ce1702
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480692"
---
# <a name="capicom_error_code-enumeration"></a>Enumeração CAPICOM \_ ERROR \_ CODE

O **tipo de \_ enumeração CAPICOM ERROR \_ CODE** define códigos de erro retornados pelo CAPICOM.

> [!Note]  
> Visual Basic Os erros da Edição de Script **retornam um valor Err.number** maior que zero. Para esses erros, os **valores de Err.Description** fornecem informações sobre a causa do erro. Além dos erros Visual Basic Scripting Edition, os erros capiCOM retornam os códigos definidos pelo **CÓDIGO DE ERRO CAPICOM \_ \_**.

 

## <a name="members"></a>Membros




| Membro | DESCRIÇÃO | Valor | 
|--------|-------------|-------|
| <strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong> | Um tipo de codificação que não é válido foi usado.<br /> A lista a seguir mostra os tipos de codificação válidos:<ul><li>CAPICOM_ENCODE_ANY</li><li>CAPICOM_ENCODE_BASE64</li><li>CAPICOM_ENCODE_BINARY</li></ul><br /> | 0x80880100 | 
| <strong>CAPICOM_E_EKU_INVALID_OID</strong> | A <a href="eku-oid.md"><strong>propriedade OID</strong></a> do objeto <a href="eku.md"><strong>EKU</strong></a> não pode ser definida porque a <a href="eku-name.md"><strong>propriedade Name</strong></a> não está definida como CAPICOM_EKU_OTHER.<br /> De definir <a href="eku-name.md"><strong>a propriedade</strong></a> Name como CAPICOM_EKU_OTHER antes de definir a <a href="eku-oid.md"><strong>propriedade OID.</strong></a><br /> | 0x80880200 | 
| <strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong> | A <a href="eku-oid.md"><strong>propriedade OID</strong></a> do <a href="eku.md"><strong>objeto EKU</strong></a> não foi inicializada. <br /> De definir a <a href="eku-name.md"><strong>propriedade Name</strong></a> como qualquer outra CAPICOM_EKU_OTHER ou definir a propriedade <strong>Name</strong> como CAPICOM_EKU_OTHER e a <a href="eku-oid.md"><strong>propriedade OID</strong></a> como um valor.<br /> | 0x80880201 | 
| <strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong> | O <a href="certificate.md"><strong>objeto</strong></a> Certificate não foi inicializado.<br /> Normalmente, esse código de erro é retornado quando um objeto <a href="certificate.md"><strong>Certificate</strong></a> é instautado, mas não associado a um certificado digital. Para associar o objeto a um certificado digital, atribua-o a um objeto <strong>Certificado</strong> existente ou chame o <a href="certificate-import.md"><strong>método Import.</strong></a><br /> | 0x80880210 | 
| <strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong> | O <a href="certificate.md"><strong>objeto</strong></a> Certificate não tem uma chave privada associada.<br /> Esse código de erro é retornado quando é feita uma tentativa de <a href="certificate.md"><strong></strong></a> assinar dados usando a chave privada do signante, mas o objeto Certificate associado ao objeto <a href="signer.md"><strong>Signer</strong></a> não pode ser usado para a operação de assinatura.<br /> | 0x80880211 | 
| <strong>CAPICOM_E_CHAIN_NOT_BUILT</strong> | O <a href="chain.md"><strong>objeto Chain</strong></a> não foi inicializado. <br /> Para inicializar o <a href="chain.md"><strong>objeto Chain,</strong></a> chame o <a href="chain-build.md"><strong>método Build.</strong></a><br /> | 0x80880220 | 
| <strong>CAPICOM_E_STORE_NOT_OPENED</strong> | O <a href="store.md"><strong>objeto Store</strong></a> não foi inicializado. <br /> Para inicializar o <a href="store.md"><strong>objeto Store,</strong></a> chame o <a href="store-open.md"><strong>método</strong></a> Open.<br /> | 0x80880230 | 
| <strong>CAPICOM_E_STORE_EMPTY</strong> | O <a href="store.md"><strong>objeto Store</strong></a> não contém nenhum objeto <a href="certificate.md"><strong>Certificate.</strong></a><br /> | 0x80880231 | 
| <strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong> | O <em>parâmetro OpenMode</em> do <a href="store-open.md"><strong>método Store.Open</strong></a> não contém um valor válido de CAPICOM_STORE_OPEN_MODE.<br /> A lista a seguir mostra os valores válidos CAPICOM_STORE_OPEN_MODE:<ul><li>CAPICOM_STORE_OPEN_READ_ONLY</li><li>CAPICOM_STORE_OPEN_READ_WRITE</li><li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li><li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li><li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li></ul><br /> | 0x80880232 | 
| <strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong> | O <em>valor SaveAs</em> passado para <a href="store-export.md"><strong>o método Export</strong></a> do objeto <a href="store.md"><strong>Store</strong></a> não era válido. <br /> A lista a seguir mostra os valores <em>válidos de SaveAs:</em><ul><li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li><li>CAPICOM_STORE_SAVE_AS_PKCS7</li></ul><br /> | 0x80880233 | 
| <strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong> | A <a href="attribute-name.md"><strong>propriedade Name</strong></a> do objeto <a href="attribute.md"><strong>Attribute</strong></a> não foi inicializada. <br /> De definir a <a href="attribute-name.md"><strong>propriedade</strong></a> Name.<br /> | 0x80880240 | 
| <strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong> | A <a href="attribute-value.md"><strong>propriedade</strong></a> Value do <a href="attribute.md"><strong>objeto Attribute</strong></a> não foi inicializada. <br /> De definir a <a href="attribute-value.md"><strong>propriedade</strong></a> Value.<br /> | 0x80880241 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong> | A <a href="attribute-name.md"><strong>propriedade Name</strong></a> do objeto <a href="attribute.md"><strong>Attribute</strong></a> não é válida. <br /> A lista a seguir mostra os nomes de atributo válidos:<ul><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li></ul><br /> | 0x80880242 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong> | A <a href="attribute-value.md"><strong>propriedade</strong></a> Value do <a href="attribute.md"><strong>objeto Attribute</strong></a> não é válida porque o tipo de dados não corresponderá ao tipo de dados indicado pela <strong>propriedade</strong> Name. <br /> Por exemplo, se a <a href="attribute-value.md"><strong>propriedade Name</strong></a> estiver definida como CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, o tipo de dados deverá ser <strong>DATE</strong>.<br /> | 0x80880243 | 
| <strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong> | O <a href="signer.md"><strong>objeto Signer</strong></a> não foi inicializado. <br /> Para inicializar o <a href="signer.md"><strong>objeto Signer,</strong></a> de definido a <a href="signer-certificate.md"><strong>propriedade</strong></a> Certificate.<br /> | 0x80880250 | 
| <strong>CAPICOM_E_SIGNER_NOT_FOUND</strong> | O signante não pode ser encontrado no <a href="signeddata.md"><strong>objeto SignedData.</strong></a> <br /> Normalmente, isso não acontece com um <a href="signeddata.md"><strong>objeto SignedData</strong></a> criado pelo CAPICOM; no entanto, se o objeto <strong>SignedData</strong> tiver sido criado por um produto de terceiros, o certificado do signante poderá não ser incluído na estrutura de #7 PKCS.<br /> | 0x80880251 | 
| <strong>CAPICOM_E_SIGNER_NO_CHAIN</strong> | Um <a href="chain.md"><strong>objeto Chain</strong></a> não pode ser encontrado no objeto <a href="signer.md"><strong>Signer.</strong></a><br /> | 0x80880252 // v2.0 | 
| <strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong> | É feita uma tentativa de usar o signante de uma maneira que não seja válida.<br /> | 0x80880253 //v2.0 | 
| <strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong> | O <a href="signeddata.md"><strong>objeto SignedData</strong></a> não foi inicializado. <br /> Para inicializar o <a href="signeddata.md"><strong>objeto SignedData,</strong></a> de definir a <a href="signeddata-content.md"><strong>propriedade Content</strong></a> ou chamar o <a href="signeddata-verify.md"><strong>método Verify.</strong></a><br /> | 0x80880260 | 
| <strong>CAPICOM_E_SIGN_INVALID_TYPE</strong> | O <a href="signeddata.md"><strong>objeto SignedData</strong></a> contém um tipo que não é válido. <br /> Normalmente, isso acontece quando é feita uma tentativa de verificar uma mensagem enveloada com um <a href="signeddata.md"><strong>objeto SignedData</strong></a> ou vice-versa.<br /> | 0x80880261 | 
| <strong>CAPICOM_E_SIGN_NOT_SIGNED</strong> | O <a href="signeddata.md"><strong>objeto SignedData</strong></a> não foi assinado. <br /> Para assinar o <a href="signeddata.md"><strong>objeto SignedData,</strong></a> chame o <a href="signeddata-sign.md"><strong>método</strong></a> Sign.<br /> | 0x80880262 | 
| <strong>CAPICOM_E_INVALID_ALGORITHM</strong> | O valor do algoritmo para <a href="algorithm-name.md"><strong>a propriedade Name</strong></a> do objeto <a href="algorithm.md"><strong>Algorithm</strong></a> não é válido. <br /> A lista a seguir mostra os valores de algoritmo válidos para a <a href="algorithm-name.md"><strong>propriedade</strong></a> Name:<ul><li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li><li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li><li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li><li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li></ul><br /> | 0x80880270 | 
| <strong>CAPICOM_E_INVALID_KEY_LENGTH</strong> | O valor de comprimento da chave <a href="algorithm-keylength.md"><strong>para a propriedade KeyLength</strong></a> do <a href="algorithm.md"><strong>objeto Algorithm</strong></a> não é válido. <br /> A lista a seguir mostra os valores de comprimento de chave válidos para a <a href="algorithm-keylength.md"><strong>propriedade KeyLength:</strong></a><ul><li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li></ul><br /> | 0x80880271 | 
| <strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong> | O <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> não foi inicializado. <br /> Para inicializar o <a href="envelopeddata.md"><strong>objeto EnvelopedData,</strong></a> descriptografe a <a href="envelopeddata-content.md"><strong>propriedade Content</strong></a> ou chame o <a href="envelopeddata-decrypt.md"><strong>método Decrypt.</strong></a><br /> | 0x80880280 | 
| <strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong> | O <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> contém um tipo que não é válido. <br /> Normalmente, isso acontece quando é feita uma tentativa de verificar uma mensagem assinada com um <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> ou vice-versa.<br /> | 0x80880281 | 
| <strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong> | Não há nenhum destinatário especificado no objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> quando o <a href="envelopeddata-encrypt.md"><strong>método Encrypt</strong></a> de um <strong>objeto EnvelopedData</strong> é chamado. <br /> Para adicionar um destinatário, chame o <a href="recipients-add.md"><strong>método Recipients.Add.</strong></a><br /> | 0x80880282 | 
| <strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong> | O destinatário não pode ser encontrado no <a href="envelopeddata.md"><strong>objeto EnvelopedData.</strong></a> <br /> Normalmente, isso não acontece com um <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> criado pelo CAPICOM; no entanto, se o objeto <strong>EnvelopedData</strong> tiver sido criado por um produto de terceiros, o certificado do destinatário poderá não ser incluído na estrutura de #7 PKCS.<br /> | 0x80880283 | 
| <strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong> | O <a href="encrypteddata.md"><strong>objeto EncryptedData</strong></a> não foi inicializado. <br /> Para inicializar o <a href="encrypteddata.md"><strong>objeto EncryptedData,</strong></a> descriptografe a <a href="encrypteddata-content.md"><strong>propriedade Content</strong></a> ou chame o <a href="encrypteddata-decrypt.md"><strong>método Decrypt.</strong></a><br /> | 0x80880290 | 
| <strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong> | O <a href="encrypteddata.md"><strong>objeto EncryptedData</strong></a> não é um tipo válido. <br /> Normalmente, isso significa que os dados estão corrompidos.<br /> | 0x80880291 | 
| <strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong> | O segredo de um <a href="encrypteddata.md"><strong>objeto EncryptedData</strong></a> não foi inicializado. <br /> Para inicializar o segredo de um <a href="encrypteddata.md"><strong>objeto EncryptedData,</strong></a> chame o <a href="encrypteddata-setsecret.md"><strong>método SetSecret.</strong></a><br /> | 0x80880292 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong> | O <a href="privatekey.md"><strong>objeto PrivateKey</strong></a> não foi inicializado.<br /> | 0x80880300 // v2.0 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong> | O <a href="privatekey.md"><strong>objeto PrivateKey</strong></a> não pode ser exportado.<br /> | 0x80880301 // v2.0 | 
| <strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong> | O <a href="encodeddata.md"><strong>objeto EncodedData</strong></a> não foi inicializado.<br /> | 0x80880320 // v2.0 | 
| <strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong> | O <a href="extension.md"><strong>objeto</strong></a> Extension não foi inicializado.<br /> | 0x80880330 // v2.0 | 
| <strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong> | A <a href="extendedproperty-propid.md"><strong>propriedade PropID</strong></a> do <a href="extendedproperty.md"><strong>objeto ExtendedProperty</strong></a> não foi inicializada.<br /> | 0x80880340 // v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_TYPE</strong> | O <em>parâmetro FindType</em> do <a href="certificates-find.md"><strong>método Certificates.Find</strong></a> não é um valor da <a href="capicom-certificate-find-type.md"><strong>enumeração CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> dados.<br /> | 0x80880350 // v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong> | A política predefinida especificada para a operação de busca não é válida.<br /> | 0x80880351 // v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong> | O <a href="signedcode.md"><strong>objeto SignedCode</strong></a> não foi inicializado.<br /> | 0x80880360 // v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_SIGNED</strong> | O <a href="signedcode.md"><strong>objeto SignedCode</strong></a> não foi assinado.<br /> Para assinar o <a href="signedcode.md"><strong>objeto SignedCode,</strong></a> chame o <a href="signedcode-sign.md"><strong>método</strong></a> Sign.<br /> | 0x80880361 // v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong> | A <a href="signedcode-description.md"><strong>propriedade Description</strong></a> do objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi inicializada.<br /> | 0x80880362 // v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong> | A <a href="signedcode-descriptionurl.md"><strong>propriedade DescriptionURL</strong></a> do <a href="signedcode.md"><strong>objeto SignedCode</strong></a> não foi inicializada.<br /> | 0x80880363 // v2.0 | 
| <strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong> | O <em>parâmetro URL</em> do método <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> não é válido.<br /> | 0x80880364 // v2.0 | 
| <strong>CAPICOM_E_HASH_NO_DATA</strong> | O <a href="hasheddata.md"><strong>objeto HashedData</strong></a> não contém nenhum dado.<br /> | 0x80880370 // v2.0 | 
| <strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong> | O tipo de conversão não é válido.<br /> | 0x80880380 // v2.0 | 
| <strong>CAPICOM_E_NOT_SUPPORTED</strong> | Não há suporte para a operação solicitada na plataforma atual. <br /> | 0x80880900 | 
| <strong>CAPICOM_E_UI_DISABLED</strong> | Ao assinar, <a href="signer-certificate.md"><strong>a propriedade Certificado</strong></a> do objeto <a href="signer.md"><strong>Signer</strong></a> não foi definida, mas o prompt para o certificado do usuário foi desabilitado. <br /> Habilita o prompt definindo a propriedade <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> do objeto <a href="signer-certificate.md"><strong></strong></a> <a href="settings.md"><strong>Configurações</strong></a> ou de definir a propriedade Certificate do <a href="signer.md"><strong>objeto Signer.</strong></a><br /> | 0x80880901 | 
| <strong>CAPICOM_E_CANCELLED</strong> | A operação foi cancelada pelo usuário. <br /> Isso acontece quando o usuário recebe uma solicitação de permissão para executar uma determinada operação, como acessar a chave privada, e o usuário cancela a operação.<br /> | 0x80880902 | 
| <strong>CAPICOM_E_NOT_ALLOWED</strong> | A operação tentada não é permitida.<br /> Por exemplo, alterar a <a href="extendedproperty-propid.md"><strong>propriedade PropID</strong></a> de <a href="extendedproperty.md"><strong>um objeto ExtendedProperty</strong></a> não será permitido se o objeto estiver anexado a um certificado.<br /> | 0x80880903 // v2.0 | 
| <strong>CAPICOM_E_OUT_OF_RESOURCE</strong> | CAPICOM ficou sem um recurso.<br /> | 0x80880904 // v2.0 | 
| <strong>CAPICOM_E_INTERNAL</strong> | Ocorreu um erro interno. <br /> Entre em contato com o Suporte Técnico da Microsoft para assistência.<br /> | 0x80880911 | 
| <strong>CAPICOM_E_UNKNOWN</strong> | Ocorreu um erro desconhecido. <br /> Colete o máximo de informações possível e entre em contato com seu fornecedor.<br /> | 0x80880999 | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




