---
title: Valores de sintaxe de aplicativo SNMP (SNMP. h)
description: Os valores de sintaxe do aplicativo SNMP são usados por aplicativos de gerenciamento que empregam a API de gerenciamento SNMP da Microsoft.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787723780d5920aafc3c37c40ea995a675943d1e45873d5f30cd8cebb77b5b64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009024"
---
# <a name="snmp-application-syntax-values"></a>Valores de sintaxe do aplicativo SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. em vez disso, use [Gerenciamento Remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

Os valores de sintaxe do aplicativo SNMP são usados por aplicativos de gerenciamento que empregam a API de gerenciamento SNMP da Microsoft.



| Constante                                                                                                                                                                                  | Descrição                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**IPAddress do ASN \_**</dt> </dl>                             | Indica uma variável de endereço IP.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**\_COUNTER32 ASN**</dt> </dl>                             | Indica uma variável de contador.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**\_GAUGE32 ASN**</dt> </dl>                                   | Indica uma variável de medidor. Essa variável descreve um tipo Unsigned32 em conformidade com RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**\_TIMEtiques ASN**</dt> </dl>                             | Indica uma variável timetiques.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**ASN \_ opaco**</dt> </dl>                                      | Indica uma variável opaca.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**\_COUNTER64 ASN**</dt> </dl>                             | Indica uma variável de contador que aumenta até atingir um valor máximo de (2 ^ 64)-1.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**\_UINTEGER32 ASN**</dt> </dl>                          | Indica uma variável de inteiro sem sinal de 32 bits. Essa variável descreve um tipo UInteger32 em conformidade com RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**\_UNSIGNED32 RFC2578 \_ ASN**</dt> </dl> | Consulte \_ GAUGE32 ASN.<br/>                                                                                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>SNMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do Protocolo SNMP](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Referência de SNMP](snmp-reference.md)
</dt> <dt>

[Constantes SNMP](snmp-constants.md)
</dt> </dl>

 

