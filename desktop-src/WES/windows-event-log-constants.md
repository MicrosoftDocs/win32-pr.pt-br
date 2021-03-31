---
title: Constantes do log de eventos do Windows (WinEvt. h)
description: O log de eventos do Windows define as seguintes constantes
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369593"
---
# <a name="windows-event-log-constants"></a>Constantes do log de eventos do Windows

O log de eventos do Windows define as seguintes constantes:

<dl> <dt>

<span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**\_máscara do \_ tipo de variante de EVT \_**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Um bitmask que você usa para mascarar o bit da matriz do tipo Variant, de modo que você pode determinar o tipo de dados do valor da variante que a estrutura de [**\_ variante de EVT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) contém.


</dt> </dl> </dd> <dt>

<span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**\_matriz de \_ tipo de variante EVT \_**
</dt> <dd> <dl> <dt>

128
</dt> <dt>



O **tipo** membro da estrutura [**de \_ variante de EVT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) tem esse bit definido se a variante contiver um ponteiro para uma matriz de valores, em vez do próprio valor.


</dt> </dl> </dd> <dt>

<span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**\_acesso de leitura EVT \_**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Permissão de controle de acesso de leitura que permite que informações sejam lidas de um log de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_acesso de gravação EVT \_**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Permissão de controle de acesso de gravação que permite que informações sejam gravadas em um log de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT \_ limpar \_ acesso**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Desmarque a permissão controle de acesso que permite que todas as informações sejam limpas de um log de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ todos os \_ acessos**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Permissão de controle de acesso All (leitura, gravação, limpeza e exclusão).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





