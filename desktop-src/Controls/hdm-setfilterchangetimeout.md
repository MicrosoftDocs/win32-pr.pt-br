---
title: Mensagem de HDM_SETFILTERCHANGETIMEOUT (commctrl. h)
description: Define o intervalo de tempo limite entre a hora em que uma alteração ocorre nos atributos de filtro e o lançamento de uma \_ notificação HDN FILTERCHANGE. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetFilterChangeTimeout do cabeçalho.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Controles de HDM_SETFILTERCHANGETIMEOUT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009617"
---
# <a name="hdm_setfilterchangetimeout-message"></a>\_Mensagem HDM SETFILTERCHANGETIMEOUT

Define o intervalo de tempo limite entre a hora em que uma alteração ocorre nos atributos de filtro e o lançamento de uma notificação [HDN \_ FILTERCHANGE](hdn-filterchange.md) . Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetFilterChangeTimeout do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

O valor de tempo limite, em milissegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do controle de filtro que está sendo modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





