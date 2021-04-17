---
description: A seguir estão os códigos de erro em tempo de execução, definidos em Cryptxml. h, que podem ser retornados pelas funções CryptXML.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Códigos de erro CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5906c406f14081844ddce042f0e170668950e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754498"
---
# <a name="cryptxml-error-codes"></a>Códigos de erro CryptXML

A seguir estão os códigos de erro em tempo de execução, definidos em Cryptxml. h, que podem ser retornados pelas funções CryptXML.



| Constante/valor                                                                                                                                                                                                                                                                             | Descrição                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**Cript \_ XML \_ E \_**</dt> <dt>0x80092101L</dt> grande </dl>                                               | O valor fornecido é muito grande.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**Cript \_ 0x80092103L \_ de \_ codificação E XML**</dt> <dt></dt> </dl>                                      | A codificação XML especificada não tem suporte.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**Cript \_ 0x80092104L \_ de \_ algoritmo E XML**</dt> <dt></dt> </dl>                                   | O algoritmo XML especificado não tem suporte.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**Cript \_ XML \_ E \_ transformar**</dt> <dt>0x80092105L</dt> </dl>                                   | A transformação especificada não tem suporte.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**Cript \_ XML \_ E \_ identificador**</dt> <dt>0x80092106L</dt> </dl>                                            | O identificador fornecido não é válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**Cript \_ 0x80092107L \_ de \_ operação XML E**</dt> <dt></dt> </dl>                                   | A operação não é válida.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**Cript \_ XML \_ E \_ \_ referência não resolvida**</dt> <dt>0x80092108L</dt> </dl> | Não é possível resolver o elemento de **referência** .<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**Cript \_ XML \_ E 0x80092109L de \_ \_ Resumo inválido**</dt> <dt></dt> </dl>                   | O valor de Digest não é válido.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**Cript \_ XML \_ E \_ \_ assinatura inválida**</dt> <dt>0x8009210AL</dt> </dl>          | O valor da assinatura não é válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**Cript \_ \_ \_ \_ Falha**</dt> de <dt>0x8009210BL</dt> de hash E XML </dl>                            | Não é possível criar ou calcular o hash.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**Cript \_ \_ \_ \_ Falha**</dt> de <dt>0x8009210CL</dt> de assinatura E XML </dl>                            | Falha na operação de assinatura criptográfica.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**Cript \_ \_ \_ \_ Falha de 0x8009210DL XML E Verify**</dt> <dt></dt> </dl>                      | Falha na verificação da assinatura.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**Cript \_ XML \_ E excesso de \_ \_ \_ assinaturas**</dt> <dt>0x8009210EL</dt> </dl>   | O número de elementos de **assinatura** no documento excedeu o limite máximo permitido para processamento.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**Cript \_ XML \_ E 0x8009210FL de \_ \_ valor inválido**</dt> <dt></dt> </dl>             | O valor de chave fornecido não é válido.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**Cript \_ XML \_ E \_ 0x80092110L \_ XML inesperados**</dt> <dt></dt> </dl>                   | Foi encontrado um XML inválido ou inesperado.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**Cript \_ 0x80092111L \_ de \_ signatário E XML**</dt> <dt></dt> </dl>                                            | Não é possível localizar a chave do signatário.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**Cript \_ XML \_ E \_ \_ \_ ID não exclusiva**</dt> <dt>0x80092112L</dt> </dl>                     | Um atributo de **ID** não exclusivo foi encontrado.<br/>                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




