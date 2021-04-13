---
title: Tipos de solicitação SNMP (SNMP. h)
description: Os tipos de solicitação SNMP são usados para descrever a operação que o serviço SNMP está solicitando que o agente de extensão execute.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455717"
---
# <a name="snmp-request-types"></a>Tipos de solicitação SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

Os tipos de solicitação SNMP são usados para descrever a operação que o serviço SNMP está solicitando que o agente de extensão execute.



| Constante/valor                                                                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_ EXTENSÃO \_ obter**</dt> <dt>SNMP \_ PDU \_ Get</dt> </dl>                       | Recupere o valor de valores das variáveis especificadas.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_ EXTENSÃO \_ obter \_ próximo**</dt> <dt>SNMP \_ PDU \_ GetNext</dt> </dl>   | Recupere o valor ou os valores do sucessor lexicográfica das variáveis especificadas.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_ EXTENSÃO \_ obter \_**</dt> o <dt>SNMP \_ PDU \_</dt> em massa/massa </dl>   | Pesquise e recupere vários valores com uma única solicitação.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**\_teste de \_ conjunto de extensões SNMP \_**</dt> </dl>                                                                           | Valide os valores das variáveis especificadas. Esta operação maximiza a probabilidade de uma operação de gravação bem-sucedida durante a solicitação de confirmação. Para obter mais informações, consulte a função [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_ conjunto de extensões \_ \_ confirmar**</dt> <dt> \_ \_ conjunto de PDU SNMP</dt> </dl> | Grave os novos valores nas variáveis especificadas.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**\_desfazer do \_ conjunto de extensões SNMP \_**</dt> </dl>                                                                           | Redefina os valores das variáveis especificadas para seus valores antes da solicitação de confirmação.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**\_limpeza do \_ conjunto de extensões SNMP \_**</dt> </dl>                                                                  | Libere os recursos alocados em operações e solicitações anteriores.<br/>                                                                                                                                                                             |



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

 

