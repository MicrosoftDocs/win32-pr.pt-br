---
description: Quando você inicializa um objeto IX500DistinguishedName com um nome distinto para identificar o assunto de uma solicitação de certificado, uma sequência de ASN (Authorized. 1) codificada de Distinguished Encoding Rules (DER) é criada.
ms.assetid: 58b05b59-2235-49bd-9543-45e786d62eaf
title: Codificando um nome de entidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa03d95497a600c3e61fdda53820fd7a9858c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010587"
---
# <a name="encoding-a-subject-name"></a>Codificando um nome de entidade

Quando você inicializa um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) com um nome distinto para identificar o assunto de uma solicitação de certificado, uma [*sequência de ASN*](/windows/desktop/SecGloss/a-gly) (Authorized. 1) codificada de [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) é criada. Por exemplo, suponha que o nome distinto da entidade consiste nos seguintes nomes distintos relativos (RDNs):<dl> E =Administrator@jdomcsc.nttest.microsoft.com  
CN = administrador  
CN = usuários  
DC = jdomcsc  
DC = nttest  
DC = Microsoft  
DC = com  
</dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">PKCS #7 a renovação do tópico ASN. 1 codificado</a> .

``` syntax
0a0d: 30 81 c4          ; SEQUENCE (c4 Bytes)
0a10: |  31 13          ; SET (13 Bytes)
0a12: |  |  30 11               ; SEQUENCE (11 Bytes)
0a14: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a16: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a20: |  |     16 03        ; IA5_STRING (3 Bytes)
0a22: |  |        63 6f 6d                                          ; com
      |  |           ; "com"
0a25: |  31 19          ; SET (19 Bytes)
0a27: |  |  30 17               ; SEQUENCE (17 Bytes)
0a29: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a2b: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a35: |  |     16 09            ; IA5_STRING (9 Bytes)
0a37: |  |        6d 69 63 72 6f 73 6f 66  74                       ; microsoft
      |  |           ; "microsoft"
0a40: |  31 16          ; SET (16 Bytes)
0a42: |  |  30 14               ; SEQUENCE (14 Bytes)
0a44: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a46: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a50: |  |     16 06            ; IA5_STRING (6 Bytes)
0a52: |  |        6e 74 74 65 73 74                                 ; nttest
      |  |           ; "nttest"
0a58: |  31 17          ; SET (17 Bytes)
0a5a: |  |  30 15               ; SEQUENCE (15 Bytes)
0a5c: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a5e: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a68: |  |     16 07            ; IA5_STRING (7 Bytes)
0a6a: |  |        6a 64 6f 6d 63 73 63                              ; jdomcsc
      |  |           ; "jdomcsc"
0a71: |  31 0e          ; SET (e Bytes)
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
0a81: |  31 16          ; SET (16 Bytes)
0a83: |  |  30 14               ; SEQUENCE (14 Bytes)
0a85: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a87: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a8a: |  |     13 0d            ; PRINTABLE_STRING (d Bytes)
0a8c: |  |        41 64 6d 69 6e 69 73 74  72 61 74 6f 72           ; Administrator
      |  |           ; "Administrator"
0a99: |  31 39          ; SET (39 Bytes)
0a9b: |     30 37               ; SEQUENCE (37 Bytes)
0a9d: |        06 09            ; OBJECT_ID (9 Bytes)
0a9f: |        |  2a 86 48 86 f7 0d 01 09  01
      |        |     ; 1.2.840.113549.1.9.1 Email Address (E)
0aa8: |        16 2a            ; IA5_STRING (2a Bytes)
0aaa: |           41 64 6d 69 6e 69 73 74  72 61 74 6f 72 40 6a 64  ; Administrator@jd
0aba: |           6f 6d 63 73 63 2e 6e 74  74 65 73 74 2e 6d 69 63  ; omcsc.nttest.mic
0aca: |           72 6f 73 6f 66 74 2e 63  6f 6d                    ; rosoft.com
      |              ; "Administrator@jdomcsc.nttest.microsoft.com"
```

Conforme discutido nos [nomes de entidades](subject-names.md), cada RDN em um nome distinto consiste em um conjunto de atributos, e cada atributo contém um OID ( [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) ) e um valor. Para entender como o objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) codifica um nome distinto, considere o nome comum CN = Users.

``` syntax
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
```

A sintaxe de transferência de DER de um objeto ASN. 1 sempre contém um tipo, comprimento e valor terceto, e cada campo no terceto contém um ou mais bytes. Quando codificados, CN = Users consistem em um OID e um valor de cadeia de caracteres. A notação decimal pontilhada do OID CN é 2.5.4.3 e o valor da cadeia de caracteres é "Users". O valor da cadeia de caracteres é representado como um tipo de dados **PRINTABLE_STRING** . O valor de tipo numérico associado a **object_id** é sempre 0x06, e o tipo numérico associado a **PRINTABLE_STRING** é sempre 0x13. O comprimento do nome comum "Users" é 0x05 bytes. O comprimento do OID é 0x03 bytes, e o valor é 0x55 0x04 0x03.

> [!Note]  
> Para converter os dois primeiros dígitos do OID 2.5.4.3 no valor hexadecimal 0x55, multiplique o primeiro dígito de OID por 40 (2 x 40) e adicione o segundo dígito (5) antes de converter para hexadecimal.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\#ASN codificado para renovação PKCS 7.1](pkcs--7-renewal-encoded-asn-1.md)
</dt> <dt>

[Solicitações de amostra](sample-requests.md)
</dt> <dt>

[Nomes de Entidades](subject-names.md)
</dt> </dl>

 

 
