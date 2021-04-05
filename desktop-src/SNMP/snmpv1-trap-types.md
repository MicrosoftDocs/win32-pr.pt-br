---
title: Tipos de interceptação SNMPv1 (SNMP. h)
description: Os tipos de interceptação SNMPv1 descrevem um conjunto predefinido de tipos de interceptação genéricos que são formatados para serem compatíveis com o padrão de PDU de interceptação SNMPv1.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824785"
---
# <a name="snmpv1-trap-types"></a>Tipos de interceptação SNMPv1

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

Os tipos de interceptação SNMPv1 descrevem um conjunto predefinido de tipos de interceptação genéricos que são formatados para serem compatíveis com o padrão de PDU de interceptação SNMPv1.



| Constante                                                                                                                                                                                                          | Descrição                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt> </dl>             | Indica uma interceptação de início frio. O agente está inicializando entidades de protocolo no modo gerenciado. Ele pode alterar objetos em sua exibição.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt> </dl>             | Indica uma interceptação de início quente. O agente está reinicializando a si mesmo, mas não alterará objetos em sua exibição.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt> </dl>                | Indica uma interceptação de vínculo abaixo. Uma interface anexada foi alterada do estado para baixo para o estado inoperante. A primeira variável na lista de associações de variáveis identifica a interface.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ linkup**</dt> </dl>                      | Indica uma interceptação de vínculo. Uma interface anexada foi alterada do estado de início para cima. A primeira variável na lista de associações de variáveis identifica a interface.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt> </dl>       | Indica uma interceptação de falha de autenticação. Uma entidade SNMP enviou uma mensagem SNMP, mas, de forma falsa, pediu para pertencer a uma comunidade conhecida.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt> </dl>    | Indica uma interceptação de perda de vizinho EGP. Um par EGP foi alterado para o estado inoperante. A primeira variável na lista de associações de variáveis identifica o endereço IP do par EGP.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt> </dl> | Indica uma interceptação específica da empresa. Ocorreu um evento extraordinário. Ele é identificado no parâmetro *specificTrap* com um valor específico da empresa.<br/>               |



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

 

