---
description: CryptXML define os seguintes limites globais no arquivo de cabeçalho Cryptxml. h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Limites de CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc56ee6459be2160efdeb8e9874e7dd0c53518d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461029"
---
# <a name="cryptxml-limits"></a>Limites de CryptXML

CryptXML define os seguintes limites globais no arquivo de cabeçalho Cryptxml. h.



| Constante/valor                                                                                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**Cript \_ 0x7FFFFFF8 \_ \_ máximo de blob XML**</dt> <dt></dt> </dl>                             | Os dados codificados não podem exceder 2 gigabytes (GB).<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**Cript \_ \_ID XML \_ máx**</dt> . <dt>256</dt> </dl>                                          | O tamanho da ID não pode exceder 256 caracteres.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**Cript \_ URI do XML \_ \_ máx**</dt> . <dt>8 \* 1024</dt> </dl>                                   | O comprimento do URI não pode exceder 8192 caracteres.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**Cript \_ \_Assinaturas XML \_ máx**</dt> . <dt>16</dt> </dl>                   | O número máximo padrão de elementos de **assinatura** por documento. Esse valor pode ser substituído especificando-se um novo máximo ao passar valores de propriedade como estruturas de [**\_ \_ propriedade XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) .<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**Cript \_ \_Transformação XML \_ Max**</dt> <dt>16</dt> </dl>                      | O número máximo de transformações, representadas por estruturas de [**\_ \_ algoritmos XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) , por referência, representadas por uma estrutura de [**\_ \_ referência XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) .<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**Cript \_ \_Valor de assinatura XML \_ \_ máx**</dt> . <dt>2048</dt> </dl> | O comprimento máximo, em bytes, de uma estrutura de [**\_ \_ assinatura XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) .<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**Cript \_ Valor de Resumo de XML \_ \_ \_ máx**</dt> . <dt>128</dt> </dl>           | O comprimento máximo, em bytes, de um resumo.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**Cript \_ \_Objetos XML \_ máx**</dt> . <dt>256</dt> </dl>                           | Usado internamente para especificar o número máximo de elementos de **objeto** permitido por assinatura.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**Cript \_ O XML \_ faz referência ao \_ Max**</dt> <dt>0x7FF8</dt> </dl>               | O número máximo de elementos de **referência** permitido.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




