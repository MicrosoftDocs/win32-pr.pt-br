---
description: Usado com operações de codificação e decodificar.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Constantes para extensões do Netscape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315d27039bf29220f1a7cdfba82baa1350da084025f436aa1b4746d7e92f5c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876746"
---
# <a name="constants-for-netscape-extensions"></a>Constantes para extensões do Netscape

As extensões do Netscape a seguir são usadas com operações de codificação e decodificar. As constantes predefinidos do Netscape e as cadeias de caracteres do identificador de objeto não são usadas diretamente com as funções de codificação ou decodificação, [**CryptEncodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject), [**CryptEncodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex), [**CryptSignAndEncodeCertificate**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate), [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)ou [**CryptDecodeObjectEx.**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) Em vez disso, essas extensões exigem o uso do *lpszStructType* mostrado.

Para obter detalhes adicionais que se aplicam a algumas extensões do Netscape, consulte os comentários após a tabela.



| Identificadores de objeto de extensão de certificado netscape                      | *Lpszstructtype*                                           | *pvStructInfo correspondente*                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL BASE do szOID \_ \_ \_ NETSCAPE"2.16.840.1.113730.1.2"<br/>           | X509 \_ ANY STRING ou \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O **membro dwValueType** é definido como CERT \_ RDN \_ IA5 \_ STRING. O **membro pbData** do membro Value aponta para uma CADEIA DE CARACTERES IA5 adicionada ao início de todos os endereços de URL  \_ relativos em um certificado. Essa extensão pode ser considerada uma otimização para reduzir o tamanho das extensões de URL.                                                                                                       |
| \_SzOID NETSCAPE \_ CA POLICY \_ \_ URL"2.16.840.1.113730.1.8"<br/>     | X509 \_ ANY STRING ou \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O **membro dwValueType** é definido como CERT \_ RDN \_ IA5 \_ STRING. O **membro** **pbData** do membro Value aponta para uma CADEIA DE CARACTERES IA5, a URL relativa ou absoluta da página da Web que descreve as políticas sob as quais o certificado \_ foi emitido.                                                                                                                                                            |
| \_SzOID NETSCAPE \_ CA \_ REVOCATION \_ URL"2.16.840.1.113730.1.4"<br/> | X509 \_ ANY STRING ou \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O **membro dwValueType** é definido como CERT \_ RDN \_ IA5 \_ STRING. O  membro **pbData** do membro Value aponta para uma CADEIA DE CARACTERES IA5 que é a URL relativa ou absoluta usada para verificar o status de revogação de certificados assinados pela autoridade de certificação à quais o certificado atual \_ pertence. [](../secgloss/c-gly.md) |
| \_SzOID NETSCAPE \_ CERT RENEWAL \_ \_ URL"2.16.840.1.113730.1.7"<br/>  | X509 \_ ANY STRING ou \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O **membro dwValueType** é definido como CERT \_ RDN \_ IA5 \_ STRING. O **membro pbData** do membro Value aponta para uma CADEIA DE CARACTERES IA5 que é a URL relativa ou absoluta de um formulário de  \_ renovação de certificado.                                                                                                                                                                                                     |
| szOID \_ NETSCAPE \_ CERT \_ SEQUENCE"2.16.840.1.113730.2.5"<br/>      | SEQUÊNCIA DE INFORMAÇÕES \_ DE CONTEÚDO \_ PKCS DE \_ \_ \_ QUALQUER                     | [**SEQUÊNCIA DE \_ INFORMAÇÕES DE CONTEÚDO DE CRIPTOGRAFIA DE \_ \_ \_ \_ QUALQUER**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| SzOID \_ NETSCAPE \_ CERT \_ TYPE"2.16.840.1.113730.1.1"<br/>          | X509 \_ BITS                                                 | [**CRYPT \_ BIT \_ BLOB**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| SzOID \_ NETSCAPE \_ COMMENT"2.16.840.1.113730.1.13"<br/>            | X509 \_ ANY STRING ou \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O **membro dwValueType** é definido como CERT \_ RDN \_ IA5 \_ STRING. O **membro pbData** do membro Value aponta para uma CADEIA DE CARACTERES IA5 que é um comentário a ser exibido quando o certificado é  \_ exibido.                                                                                                                                                                                                         |
| \_SzOID NETSCAPE \_ REVOCATION \_ URL"2.16.840.1.113730.1.3"<br/>     | X509 \_ ANY STRING ou \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O **membro dwValueType** é definido como CERT \_ RDN \_ IA5 \_ STRING. O **membro pbData** do membro Value aponta para uma CADEIA DE CARACTERES IA5 que é uma URL relativa ou absoluta usada para verificar o status de  \_ revogação do certificado.                                                                                                                                                                              |
| szOID \_ NETSCAPE \_ SSL \_ SERVER \_ NAME"2.16.840.1.113730.1.12"<br/>  | X509 \_ ANY STRING ou \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O **membro dwValueType** é definido como CERT \_ RDN \_ IA5 \_ STRING. O **membro pbData** do membro Value aponta para uma CADEIA DE CARACTERES IA5 que é uma expressão de shell usada para corresponder ao nome do host do servidor SSL usando esse  \_ certificado.                                                                                                                                                                       |



 

Para todas as funções de codificação que usam x509 ANY STRING ou \_ \_ x5O9 \_ UNICODE \_ ANY STRING \_ **lpszStructType**, X509 ANY STRING será usado se o formato de cadeia de caracteres no membro pbData do valor for \_ \_ [*ASCII*](../secgloss/a-gly.md)e X509 UNICODE ANY STRING   \_ \_ \_ for usado se o formato de cadeia de caracteres for UNICODE. No caso Unicode, a cadeia de caracteres deve ser convertida em uma CADEIA DE CARACTERES IA5 antes da codificação definindo o membro \_ **dwValueType** da estrutura [**CERT NAME \_ \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) como CERT \_ RDN \_ IA5 \_ STRING.

Para funções de decodificação, o usuário seleciona o formato da cadeia de caracteres de saída. Use X509 ANY STRING se o formato de cadeia de caracteres desejado for \_ ASCII e X509 UNICODE ANY STRING se o formato de cadeia de caracteres desejado \_ \_ for \_ \_ Unicode.

Para a extensão de URL de RENOVAÇÃO de CERTIFICADO szOID NETSCAPE, a estrutura de dados contém uma URL relativa ou absoluta que \_ aponta para um formulário de \_ \_ \_ renovação de certificado. O formulário de renovação será acessado com um método HTTP GET usando uma URL que seja a concatenação da URL de renovação e do número de série do certificado. O número de série do certificado é codificado como uma cadeia de caracteres de dígitos hexadecimais ASCII. Por exemplo, se netscape-base-https:// url for uma *URL* da autoridade de certificação /, o netscape-cert-renewal-url será cgi-bin/check-renew.cgi?, e o número de série do certificado for 173420, a URL resultante será:*URL* da autoridade de certificação do https:// /cgi-bin/check-renew.cgi?02a56c. O documento retornado deve ser um formulário HTML que permitirá que o usuário solicite uma renovação de seu certificado.

Para a extensão szOID NETSCAPE CERT SEQUENCE usando A CODIFICAÇÃO \_ \_ \_ ASN X509, o certificado é codificado como uma estrutura \_ \_ PKCS CONTENT \_ \_ INFO que envolve uma sequência de ANY. O valor do membro **contentType** é **pszObjId,** enquanto o campo de conteúdo é a seguinte estrutura:

SequenceOfAny ::= SEQUENCE OF ANY

Os [**\_ \_ BLOB de CRYPT DER**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))na SEQUÊNCIA DE INFORMAÇÕES DE CONTEÚDO DE [**\_ \_ \_ \_ \_ CRIPTOGRAFIA**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)DO ponto de membro **rgValue** de ANY para certificados X509 codificados.

Para extensões szOID \_ NETSCAPE \_ CERT \_ TYPE, os bits a seguir são definidos.



| Valor de bit | Tipo correspondente                      |
|-----------|-----------------------------------------|
| 0x80      | TIPO DE \_ CERTIFICADO DE \_ \_ AUTH DO CLIENTE \_ \_ NETSCAPE SSL |
| 0x40      | TIPO DE CERTIFICADO DE \_ \_ \_ AUTH DO \_ SERVIDOR NETSCAPE SSL \_ |
| 0x04      | TIPO DE \_ CERTIFICADO DE AUTORIDADE DE \_ \_ CERTIFICAÇÃO DO \_ NETSCAPE SSL           |



 

Para as extensões de URL de REVOGAÇÃO do szOID NETSCAPE, uma URL relativa ou absoluta pode ser usada para verificar o status de revogação \_ \_ de um \_ certificado. A verificação de revogação será executada como um método HTTP GET usando uma URL que é a concatenação de revogação-URL e número de série de certificado. O número de série do certificado é codificado como uma cadeia de caracteres de dígitos hexadecimais ASCII. Por exemplo, se netscape-base-url for https: \/ /www.certs-r-us.com/, netscape-revocation-url será cgi-bin/check-rev.cgi?, e o número de série do certificado for 173420, a URL resultante será: https: \/ /www.certs-r-us.com/cgi-bin/check-rev.cgi?02a56c.

O servidor deve retornar um documento com um Content-Type de application/x-netscape-revocation. O documento deverá conter um único dígito ASCII, "1" se o certificado não for válido no momento e "0" se ele for válido no momento.

Observe que, para todas as URLs que incluem o número de série do certificado, o número de série será codificado como uma cadeia de caracteres que consiste em um número de dígitos hexadecimais. Se o número de dígitos significativos for ímpar, a cadeia de caracteres terá um único zero à esquerda para garantir que um número único de dígitos seja gerado.

 

 
