---
title: Códigos de erro SNMP (SNMP. h)
description: A Microsoft implementa os seguintes códigos de erro SNMP que são definidos pela especificação do SNMPv2C.
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c1ec7a25490737dd31b2962c09d2e0f36c72d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008970"
---
# <a name="snmp-error-codes"></a>Códigos de erro SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

A Microsoft implementa os seguintes códigos de erro SNMP que são definidos pela especificação do SNMPv2C.



| Constante/valor                                                                                                                                                                                                                                                                              | Descrição                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOERROR**</dt> <dt>0</dt> </dl>                                      | O agente relata que nenhum erro ocorreu durante a transmissão.<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ TOOBIG**</dt> <dt>1</dt> </dl>                                         | O agente não pôde posicionar os resultados da operação SNMP solicitada em uma única mensagem SNMP.<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_**</dt> <dt>2</dt> </dl>                             | A operação SNMP solicitada identificou uma variável desconhecida.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ BADVALUE**</dt> <dt>3</dt> </dl>                                   | A operação SNMP solicitada tentou alterar uma variável, mas especificou um erro de sintaxe ou valor.<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ ReadOnly**</dt> <dt>4</dt> </dl>                                   | A operação SNMP solicitada tentou alterar uma variável que não tem permissão para ser alterada, de acordo com o perfil da Comunidade da variável.<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ GENERR**</dt> <dt>5</dt> </dl>                                         | Um erro diferente de um dos listados aqui ocorreu durante a operação SNMP solicitada.<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NoAccess**</dt> <dt>6</dt> </dl>                                   | A variável SNMP especificada não está acessível.<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ incorretotype**</dt> <dt>7</dt> </dl>                                | O valor especifica um tipo que é inconsistente com o tipo necessário para a variável.<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGLENGTH**</dt> <dt>8</dt> </dl>                          | O valor especifica um comprimento que é inconsistente com o comprimento necessário para a variável.<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGENCODING**</dt> <dt>9</dt> </dl>                    | O valor contém uma codificação de uma (ASN. 1) de sintaxe abstrata que é inconsistente com a marca ASN. 1 do campo.<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ incorretovalue**</dt> <dt>10</dt> </dl>                            | O valor não pode ser atribuído à variável.<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ nocreation**</dt> <dt>11</dt> </dl>                            | A variável não existe e o agente não pode criá-la.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INconsistent**</dt> <dt>12</dt> </dl>       | O valor é inconsistente com os valores de outros objetos gerenciados.<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ RESOURCEUNAVAILABLE**</dt> <dt>13</dt> </dl> | A atribuição do valor à variável requer a alocação de recursos que não estão disponíveis no momento.<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ COMMITFAILED**</dt> <dt>14</dt> </dl>                      | Não ocorreu nenhum erro de validação, mas nenhuma variável foi atualizada.<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ UNDOFAILED**</dt> <dt>15</dt> </dl>                            | Não ocorreu nenhum erro de validação. Algumas variáveis foram atualizadas porque não foi possível desfazer a atribuição.<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ AUTHORIZATIONERROR**</dt> <dt>16</dt> </dl>    | Ocorreu um erro de autorização.<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**SNMP \_ ERRORSTATUS não \_ gravável**</dt> <dt>17</dt> </dl>                         | A variável existe, mas o agente não pode modificá-la.<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INconsistent**</dt> <dt>18</dt> </dl>          | A variável não existe; o agente não pode criá-lo porque a instância do objeto nomeado está inconsistente com os valores de outros objetos gerenciados.<br/> |



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
</dt> </dl>

 

