---
description: O tipo de dados do identificador de objeto é codificado em um terceto TLV que começa com um valor de marca de 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: IDENTIFICADOR DE OBJETO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35c2bf64424fa158eef3c666743142d5ec5a65108e3def28c43194d2eaf5adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903780"
---
# <a name="object-identifier"></a>IDENTIFICADOR DE OBJETO

O tipo de dados do **identificador de objeto** é codificado em um terceto TLV que começa com um valor de **marca** de 0x06. Cada inteiro de um identificador de objeto decimal (OID) pontilhado é codificado de acordo com as seguintes regras:

-   Os primeiros dois nós do OID são codificados em um único byte. O primeiro nó é multiplicado pelo decimal 40 e o resultado é adicionado ao valor do segundo nó.
-   Valores de nó menores ou iguais a 127 são codificados em um byte.
-   Valores de nó maiores ou iguais a 128 são codificados em vários bytes. O bit 7 do byte mais à esquerda é definido como um. Bits 0 a 6 de cada byte contêm o valor codificado.

Esses pontos são mostrados pela ilustração a seguir.

![codificação der do tipo de dados do identificador de objeto](images/der-tlv-oid.png)

O exemplo a seguir mostra como o atributo **ClientID** é codificado em uma solicitação de certificado.

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

 

 



