---
description: O CryptXML oferece suporte nativo aos URIs listados abaixo.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Algoritmos criptográficos de assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796364"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a>Algoritmos criptográficos de assinatura digital XML

O CryptXML oferece suporte nativo aos URIs listados abaixo. Se o suporte for necessário para algoritmos criptográficos e transformações que não fazem parte do suporte nativo, você poderá usar a [API de criptografia: próxima geração](../seccng/cng-portal.md) e [extensões criptográficas de assinatura digital XML](xml-digital-signature-cryptographic-extensions.md) para dar suporte a novos algoritmos.

## <a name="supported-uris"></a>URIs com suporte

Métodos de resumo



| Constante                                 | Valor do URI                                                   |
|------------------------------------------|-------------------------------------------------------------|
| wszURI \_ xmlns \_ DIGSIG \_ SHA1<br/>   | "https://www.w3.org/2000/09/xmldsig\#sha1"<br/>        |
| wszURI \_ xmlns \_ DIGSIG \_ SHA256<br/> | "https://www.w3.org/2001/04/xmlenc\#sha256"<br/>       |
| wszURI \_ xmlns \_ DIGSIG \_ Sha384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#sha384"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ SHA512<br/> | "https://www.w3.org/2001/04/xmlenc\#sha512"<br/>       |



 

Métodos de assinatura



| Constante                                        | Valor do URI                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#rsa-sha1"<br/>          |
| wszURI \_ xmlns \_ DIGSIG \_ DSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#dsa-sha1"<br/>          |
| wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA256<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ RSA \_ Sha384<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA512<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA1<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA256<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ Sha384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA512<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA1<br/>    | "https://www.w3.org/2000/09/xmldsig\#hmac-sha1"<br/>         |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA256<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"<br/>  |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ Sha384<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"<br/>  |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA512<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"<br/>  |



 

 

 
