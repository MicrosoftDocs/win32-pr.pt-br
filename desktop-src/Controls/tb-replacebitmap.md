---
title: TB_REPLACEBITMAP mensagem (Commctrl.h)
description: Substitui um bitmap existente por um novo bitmap.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- TB_REPLACEBITMAP controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11dd964691b8b854feb09f93bc03673c46103bb34842e326e0f433cfd1fcc77f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968046"
---
# <a name="tb_replacebitmap-message"></a>Mensagem DE TB \_ REPLACEBITMAP

Substitui um bitmap existente por um novo bitmap.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) que contém as informações do bitmap a ser substituído e o novo bitmap.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





