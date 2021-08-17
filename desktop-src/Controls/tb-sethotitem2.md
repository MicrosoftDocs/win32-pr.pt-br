---
title: TB_SETHOTITEM2 mensagem (Commctrl.h)
description: TB_SETHOTITEM2 mensagem – define o item quente em uma barra de ferramentas.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f4bb1e560e2be2b6952406d548215d60f2c2974e57b2388580da7453b51c184
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318816"
---
# <a name="tb_sethotitem2-message"></a>Mensagem TB \_ SETHOTITEM2

Define o item quente em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item que ficará quente. Se esse valor for -1, nenhum dos itens ficará quente.

</dd> <dt>

*lParam* 
</dt> <dd>Uma combinação de sinalizadores \_ XXX HICF. Consulte <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do item quente anterior ou -1 se não houver nenhum item quente.

## <a name="remarks"></a>Comentários

O comportamento dessa mensagem não está definido para barras de ferramentas que não têm o [**estilo TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





