---
title: HDM_SETFILTERCHANGETIMEOUT mensagem (Commctrl.h)
description: Define o intervalo de tempo entre o momento em que uma alteração ocorre nos atributos de filtro e a postagem de uma notificação \_ FILTERCHANGE do HDN. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Header SetFilterChangeTimeout.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT controles de Windows mensagem
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
ms.openlocfilehash: 23b5f8df12a7f30baa5f8b7d4bf15698b30cfbb6619fb71a81d4977b259c318b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435856"
---
# <a name="hdm_setfilterchangetimeout-message"></a>Mensagem HDM \_ SETFILTERCHANGETIMEOUT

Define o intervalo de tempo entre o momento em que uma alteração ocorre nos atributos de filtro e a postagem de uma notificação [ \_ FILTERCHANGE do HDN.](hdn-filterchange.md) Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ Header SetFilterChangeTimeout.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

O valor de tempo limite, em milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do controle de filtro que está sendo modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





