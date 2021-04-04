---
description: Usado com operações de codificação e decodificação.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Constantes para extensões do Netscape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06999a879d0d289bb95cdb8ba5506200154d60e4
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103837917"
---
# <a name="constants-for-netscape-extensions"></a>Constantes para extensões do Netscape

As seguintes extensões do Netscape são usadas com operações de codificação e decodificação. As constantes predefinidas do Netscape e as cadeias de caracteres do identificador de objeto não são usadas diretamente com as funções de codificação ou decodificação, [**CryptEncodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject), [**CryptEncodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex), [**CryptSignAndEncodeCertificate**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate), [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)ou [**CryptDecodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex). Em vez disso, essas extensões exigem o uso do *lpszStructType* mostrado.

Para obter detalhes adicionais que se aplicam a algumas extensões do Netscape, consulte os comentários após a tabela.



| Identificadores de objeto de extensão de certificado do Netscape                      | *lpszStructType*                                           | *PvStructInfo* correspondente                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_URL base do szOID Netscape \_ \_ "2.16.840.1.113730.1.2"<br/>           | X509 \_ qualquer cadeia \_ de caracteres ou X509 \_ Unicode \_ Any \_<br/> | [**Certificado \_ \_valor de nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O membro **dwValueType** é definido como \_ cadeia de \_ caracteres IA5 do certificado \_ . O membro **pbData** do membro de **valor** aponta para uma \_ cadeia de caracteres IA5 adicionada ao início de todos os endereços de URL relativos em um certificado. Essa extensão pode ser considerada uma otimização para reduzir o tamanho das extensões de URL.                                                                                                       |
| \_ \_ URL da política de AC do szOID Netscape \_ \_ "2.16.840.1.113730.1.8"<br/>     | X509 \_ qualquer cadeia \_ de caracteres ou X509 \_ Unicode \_ Any \_<br/> | [**Certificado \_ \_valor de nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O membro **dwValueType** é definido como \_ cadeia de \_ caracteres IA5 do certificado \_ . O membro **pbData** do membro de **valor** aponta para uma \_ cadeia de caracteres IA5, a URL relativa ou absoluta da página da Web que descreve as políticas sob as quais o certificado foi emitido.                                                                                                                                                            |
| \_URL de \_ revogação da AC do szOID Netscape \_ \_ "2.16.840.1.113730.1.4"<br/> | X509 \_ qualquer cadeia \_ de caracteres ou X509 \_ Unicode \_ Any \_<br/> | [**Certificado \_ \_valor de nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O membro **dwValueType** é definido como \_ cadeia de \_ caracteres IA5 do certificado \_ . O membro **pbData** do membro de **valor** aponta para uma \_ cadeia de caracteres IA5 que é a URL relativa ou absoluta usada para verificar o status de revogação de certificados assinados pela [*autoridade de certificação*](../secgloss/c-gly.md) à qual o certificado atual pertence. |
| URL de renovação de certificado do szOID \_ Netscape \_ \_ \_ "2.16.840.1.113730.1.7"<br/>  | X509 \_ qualquer cadeia \_ de caracteres ou X509 \_ Unicode \_ Any \_<br/> | [**Certificado \_ \_valor de nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O membro **dwValueType** é definido como \_ cadeia de \_ caracteres IA5 do certificado \_ . O membro **pbData** do membro de **valor** aponta para uma \_ cadeia de caracteres IA5 que é a URL relativa ou absoluta de um formulário de renovação de certificado.                                                                                                                                                                                                     |
| szOID a \_ sequência de certificados do Netscape \_ \_ "2.16.840.1.113730.2.5"<br/>      | \_ \_ \_ sequência de informações de conteúdo PKCS \_ de \_ qualquer                     | [**\_ \_ sequência de informações de conteúdo cript. \_ \_ de \_ qualquer**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| \_tipo de certificado szOID Netscape \_ \_ "2.16.840.1.113730.1.1"<br/>          | \_Bits X509                                                 | [**\_blob de bits cript \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| szOID \_ o \_ Comentário do Netscape "2.16.840.1.113730.1.13"<br/>            | X509 \_ qualquer cadeia \_ de caracteres ou X509 \_ Unicode \_ Any \_<br/> | [**Certificado \_ \_valor de nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O membro **dwValueType** é definido como \_ cadeia de \_ caracteres IA5 do certificado \_ . O membro **pbData** do membro de **valor** aponta para uma \_ cadeia de caracteres IA5 que é um comentário a ser exibido quando o certificado é exibido.                                                                                                                                                                                                         |
| \_URL de revogação do szOID Netscape \_ \_ "2.16.840.1.113730.1.3"<br/>     | X509 \_ qualquer cadeia \_ de caracteres ou X509 \_ Unicode \_ Any \_<br/> | [**Certificado \_ \_valor de nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O membro **dwValueType** é definido como \_ cadeia de \_ caracteres IA5 do certificado \_ . O membro **pbData** do membro de **valor** aponta para uma \_ cadeia de caracteres IA5 que é uma URL relativa ou absoluta usada para verificar o status de revogação do certificado.                                                                                                                                                                              |
| \_ \_ \_ nome do servidor SSL do szOID Netscape \_ "2.16.840.1.113730.1.12"<br/>  | X509 \_ qualquer cadeia \_ de caracteres ou X509 \_ Unicode \_ Any \_<br/> | [**Certificado \_ \_valor de nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). O membro **dwValueType** é definido como \_ cadeia de \_ caracteres IA5 do certificado \_ . O membro **pbData** do membro de **valor** aponta para uma \_ cadeia de caracteres IA5 que é uma expressão de shell usada para corresponder o nome do host do servidor SSL usando esse certificado.                                                                                                                                                                       |



 

Para todas as funções de codificação que usam a \_ cadeia de caracteres X509 Any \_ ou X5O9 \_ Unicode \_ Any \_ String **lpszStructType**, o X509 \_ Any \_ String será usado se o formato da cadeia de caracteres no membro **pbData** do membro do **valor** for [*ASCII*](../secgloss/a-gly.md)e \_ o X509 Unicode \_ Any \_ for usado se o formato da cadeia de caracteres for Unicode. No caso do Unicode, a cadeia de caracteres deve ser convertida em uma \_ cadeia de caracteres IA5 antes da codificação, definindo o membro **dwValueType** da estrutura de [**valor do \_ nome \_ do certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) como \_ cadeia de \_ caracteres IA5 do certificado \_ .

Para funções de decodificação, o usuário seleciona o formato da cadeia de caracteres de saída. Use X509 \_ Any \_ String se o formato de cadeia de caracteres desejado for ASCII e X509 \_ Unicode \_ Any \_ String se o formato de cadeia de caracteres desejado for Unicode.

Para a extensão de URL de renovação de certificado do szOID \_ Netscape \_ \_ \_ , a estrutura de dados contém uma URL relativa ou absoluta que aponta para um formulário de renovação de certificado. O formulário de renovação será acessado com um método HTTP GET usando uma URL que é a concatenação da URL de renovação e do número de série de certificados. O número de série de certificados é codificado como uma cadeia de caracteres hexadecimais ASCII. Por exemplo, se o Netscape-base-URL for https://da *autoridade de certificação*/, o Netscape-CERT-Renew-URL será cgi-bin/check-Renew. cgi? e o número de série do certificado for 173420, a URL resultante será: https://URL da autoridade de *certificação*/cgi-bin/check-Renew.cgi? 02a56c. O documento retornado deve ser um formulário HTML que permitirá que o usuário solicite uma renovação de seu certificado.

Para a extensão de sequência de certificados do szOID \_ Netscape \_ \_ usando \_ \_ a codificação ASN X509, o certificado é codificado como uma \_ \_ estrutura de informações de conteúdo PKCS encapsulando uma sequência de qualquer. O valor do membro **ContentType** é **pszObjId**, enquanto o campo Content é a seguinte estrutura:

SequenceOfAny:: = sequência de qualquer

Os s de [**\_ \_ blob codificado**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))em cript [**na \_ \_ \_ sequência de informações de conteúdo cript \_ de \_ qualquer ponto de**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)membro **rgValue** para certificados X509 codificados.

Para extensões de tipo de certificado do szOID \_ Netscape \_ \_ , os seguintes bits são definidos.



| Valor de bit | Tipo correspondente                      |
|-----------|-----------------------------------------|
| 0x80      | \_tipo de \_ \_ certificado de autenticação do cliente SSL \_ do \_ Netscape |
| 0x40      | \_tipo de \_ certificado de autenticação do servidor SSL do Netscape \_ \_ \_ |
| 0x04      | \_tipo de \_ certificado de autoridade de certificação SSL do \_ Netscape \_           |



 

Para as \_ extensões de URL de revogação do szOID Netscape \_ \_ , uma URL relativa ou absoluta pode ser usada para verificar o status de revogação de um certificado. A verificação de revogação será executada como um método HTTP GET usando uma URL que é a concatenação de URL de revogação e número de série de certificados. O número de série de certificados é codificado como uma cadeia de caracteres hexadecimais ASCII. Por exemplo, se o Netscape-base-URL for https: \/ /www.certs-r-us.com/, o Netscape-rerevocation-URL será cgi-bin/check-Rev. cgi? e o número de série do certificado for 173420, a URL resultante será: https: \/ /www.certs-r-us.com/cgi-bin/check-Rev.cgi?02a56c.

O servidor deve retornar um documento com um tipo de conteúdo de application/x-Netscape-Revocation. O documento deve conter um único dígito ASCII, "1" se o certificado não for válido no momento e "0" se ele for válido no momento.

Observe que para todas as URLs que incluem o número de série do certificado, o número de série será codificado como uma cadeia de caracteres que consiste em um número par de dígitos hexadecimais. Se o número de dígitos significativos for ímpar, a cadeia de caracteres terá um único zero à esquerda para garantir que um número par de dígitos seja gerado.

 

 
