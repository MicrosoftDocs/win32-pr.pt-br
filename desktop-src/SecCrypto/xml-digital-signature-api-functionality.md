---
description: O CryptXML fornece um conjunto de APIs de baixo nível que permite que os aplicativos criem e verifiquem assinaturas envelopadas, enveloping e desanexadas. Você pode usar o CryptXML para criar e verificar o conteúdo armazenado em elementos de objeto de assinatura, incluindo manifestos.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Funcionalidade de API de assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755034"
---
# <a name="xml-digital-signature-api-functionality"></a>Funcionalidade de API de assinatura digital XML

O CryptXML fornece um conjunto de APIs de baixo nível que permite que os aplicativos criem e verifiquem assinaturas envelopadas, enveloping e desanexadas. Você pode usar o CryptXML para criar e verificar o conteúdo armazenado em elementos de objeto de assinatura, incluindo manifestos. Uma chave pública/privada, compartilhada ou um certificado [*X. 509*](../secgloss/x-gly.md) ou uma cadeia de certificados pode ser usada para assinar e verificar a [*assinatura digital*](../secgloss/d-gly.md)XML.

Os aplicativos que usam CryptXML para verificar referências externas (referências que se destinam a um documento ou arquivo externo fora do contexto do documento) devem resolver os URIs externos e recuperar os dados a serem resumidos.

Para obter informações sobre os algoritmos de criptografia com suporte do CryptXML, consulte [algoritmos criptográficos de assinatura digital XML](xml-digital-signature-cryptographic-algorithms.md).

O CryptXML fornece suporte para os algoritmos de canonização com os seguintes identificadores.



| Constante                                              | Valor do URI                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| \_c14n de canonização wszURI \_<br/>             | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315"<br/>               |
| \_C14NC de canonização wszURI \_<br/>            | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"<br/> |
| wszURI \_ canonização \_ EXSLUSIVE \_ c14n<br/>  | "https://www.w3.org/2001/10/xml-exc-c14n\#"<br/>                      |
| wszURI \_ canonização \_ EXSLUSIVE \_ C14NC<br/> | "https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"<br/>          |



 

CryptXML fornece suporte para a transformação de assinatura envelopada.



| Constante                                       | Valor do URI                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| \_transformação xmlns \_ wszURI \_ envelopada<br/> | "https://www.w3.org/2000/09/xmldsig\#enveloped-signature"<br/> |



 

Por padrão, o CryptXML não oferece suporte a transformações XPath ou XSLT. Se necessário, os aplicativos podem implementar essas transformações sobre CryptXML.

 

 
