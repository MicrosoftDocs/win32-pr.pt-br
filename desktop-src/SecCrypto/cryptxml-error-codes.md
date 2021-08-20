---
description: A seguir estão os códigos de erro de tempo de run, definidos em Cryptxml.h, que podem ser retornados pelas funções CryptXML.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Códigos de erro CryptXML (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb4b06070ca77f8b55f96d3e6c4732abc22c26970b83b6a70c720b7bade8a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767973"
---
# <a name="cryptxml-error-codes"></a>Códigos de erro cryptXML

A seguir estão os códigos de erro de tempo de run, definidos em Cryptxml.h, que podem ser retornados pelas funções CryptXML.



| Constante/valor                                                                                                                                                                                                                                                                             | Descrição                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**CRYPT \_ XML \_ E \_ LARGE**</dt> <dt>0x80092101L</dt> </dl>                                               | O valor fornecido é muito grande.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**CRYPT \_ CODIFICAÇÃO \_ \_ XML**</dt> <dt>0x80092103L</dt> </dl>                                      | Não há suporte para a codificação XML especificada.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**CRYPT \_ XML \_ E \_ ALGORITHM**</dt> <dt>0x80092104L</dt> </dl>                                   | Não há suporte para o Algoritmo XML especificado.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**CRYPT \_ XML \_ E \_ TRANSFORM**</dt> <dt>0x80092105L</dt> </dl>                                   | Não há suporte para a transformação especificada.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**CRYPT \_ XML \_ E \_ HANDLE**</dt> <dt>0x80092106L</dt> </dl>                                            | O handle fornecido não é válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**CRYPT \_ XML \_ E \_ OPERATION**</dt> <dt>0x80092107L</dt> </dl>                                   | A operação não é válida.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**CRYPT \_ REFERÊNCIA \_ XML E \_ UNRESOLVED \_**</dt> <dt>0x80092108L</dt> </dl> | Não é possível resolver o **elemento** Reference.<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**CRYPT \_ XML \_ E \_ DIGEST \_ INVÁLIDO**</dt> <dt>0x80092109L</dt> </dl>                   | O valor de resumo não é válido.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ SIGNATURE**</dt> <dt>0x8009210AL</dt> </dl>          | O valor da assinatura não é válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**CRYPT \_ FALHA \_ DE HASH \_ XML \_ E**</dt> <dt>0x8009210BL</dt> </dl>                            | Não é possível criar ou calcular o hash.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**CRYPT \_ FALHA \_ DE \_ SINAL \_ XML E**</dt> <dt>0x8009210CL</dt> </dl>                            | Falha na operação de assinatura criptográfica.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**CRYPT \_ XML \_ E \_ VERIFY \_ FAILED**</dt> <dt>0x8009210DL</dt> </dl>                      | Falha na verificação de assinatura.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**CRYPT \_ XML \_ E \_ MUITAS \_ \_ ASSINATURAS**</dt> <dt>0x8009210EL</dt> </dl>   | O número de **elementos Signature** no documento excedeu o limite máximo permitido para processamento.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**CRYPT \_ XML \_ E \_ \_ KEYVALUE INVÁLIDO**</dt> <dt>0x8009210FL</dt> </dl>             | O valor da chave que foi fornecido não é válido.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**CRYPT \_ XML \_ E \_ UNEXPECTED \_ XML**</dt> <dt>0x80092110L</dt> </dl>                   | XML inválido ou inesperado foi encontrado.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**CRYPT \_ XML \_ E \_ SIGNER**</dt> <dt>0x80092111L</dt> </dl>                                            | Não é possível localizar a chave do signante.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**CRYPT \_ XML \_ E \_ \_ \_ ID NÃO EXCLUSIVA**</dt> <dt>0x80092112L</dt> </dl>                     | Um atributo de **ID nãounique** foi encontrado.<br/>                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 




