---
title: Valores de tipo de PDU (SNMP. h)
description: Os valores do tipo PDU são usados no \_ campo tipo PDU da PDU para descrever seu tipo.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e9346c313efccda6d3635da51919f52fae37dd901cc73cf1f119bffdf9c22c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009204"
---
# <a name="pdu-type-values"></a>Valores de tipo de PDU

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. em vez disso, use [Gerenciamento Remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

Os valores do tipo PDU são usados no **campo \_ tipo PDU** da PDU para descrever seu tipo.



| Constante                                                                                                                                                                   | Descrição                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**\_Get SNMP PDU \_**</dt> </dl>                | Pesquisar e recuperar um valor de uma variável SNMP especificada.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**o SNMP \_ PDU \_ GetNext**</dt> </dl>    | Pesquise e recupere o valor de uma variável SNMP sem saber o nome exato da variável.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**\_resposta de PDU de SNMP \_**</dt> </dl> | Responder a uma solicitação do SNMP \_ PDU \_ Get ou SNMP \_ PDU \_ GetNext.<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**\_conjunto de PDU SNMP \_**</dt> </dl>                | Armazene um valor em uma variável SNMP especificada.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**\_V1TRAP de PDU SNMP \_**</dt> </dl>       | Indica que a interceptação de PDU está formatada para estar em conformidade com o padrão SNMPv1.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**SNMP \_ PDU \_ GetBulk**</dt> </dl>    | Pesquise e recupere vários valores com uma única solicitação.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**informar sobre o SNMP \_ PDU \_**</dt> </dl>       | Indica uma PDU de solicitação de informe.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**\_interceptação de PDU SNMP \_**</dt> </dl>             | Alerta o sistema de gerenciamento para um evento extraordinário sob o SNMPv2C.<br/>                             |



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

 

