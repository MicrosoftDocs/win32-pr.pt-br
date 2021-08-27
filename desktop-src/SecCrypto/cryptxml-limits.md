---
description: CryptXML define os seguintes limites globais no arquivo de header Cryptxml.h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Limites de CryptXML (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a0dcdf5dc8f8bd9efed4dcdb15ca316ecb1645e5775f3d714f46c6835b3a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100916"
---
# <a name="cryptxml-limits"></a>Limites de CryptXML

CryptXML define os seguintes limites globais no arquivo de header Cryptxml.h.



| Constante/valor                                                                                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**CRYPT \_ XML \_ BLOB \_ MAX**</dt> <dt>0x7FFFFFF8</dt> </dl>                             | Os dados codificados não podem exceder 2 GB (gigabytes).<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**CRYPT \_ ID XML \_ \_ MAX**</dt> <dt>256</dt> </dl>                                          | O comprimento da ID não pode exceder 256 caracteres.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**CRYPT \_ XML \_ URI \_ MAX**</dt> <dt>8 \* 1024</dt> </dl>                                   | O comprimento do URI não pode exceder 8192 caracteres.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**CRYPT \_ XML \_ SIGNATURES \_ MAX**</dt> <dt>16</dt> </dl>                   | O número máximo padrão de **elementos signature** por documento. Esse valor pode ser substituído especificando um novo máximo ao passar valores de propriedade como estruturas [**CRYPT \_ XML \_ PROPERTY.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property)<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**CRYPT \_ XML \_ TRANSFORM \_ MAX**</dt> <dt>16</dt> </dl>                      | O número máximo de transformares, representado por estruturas [**CRYPT \_ XML \_ ALGORITHM,**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) por referência, representadas por uma estrutura [**CRYPT XML \_ \_ REFERENCE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference)<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**CRYPT \_ VALOR DE ASSINATURA XML \_ \_ \_ MAX**</dt> <dt>2048</dt> </dl> | O comprimento máximo, em bytes, de uma estrutura [**CRYPT \_ XML \_ SIGNATURE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature)<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**CRYPT \_ VALOR \_ XML DIGEST \_ \_ MÁX.**</dt> <dt>128</dt> </dl>           | O comprimento máximo, em bytes, de um resumo.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**CRYPT \_ XML \_ OBJECTS \_ MAX**</dt> <dt>256</dt> </dl>                           | Usado internamente para especificar o número máximo de elementos **Object** permitidos por assinatura.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**CRYPT \_ XML \_ REFERENCES \_ MAX**</dt> <dt>0x7FF8</dt> </dl>               | O número máximo de elementos **reference** permitidos.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 




