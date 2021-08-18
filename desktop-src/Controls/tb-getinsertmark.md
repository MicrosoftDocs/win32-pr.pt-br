---
title: Mensagem de TB_GETINSERTMARK (commctrl. h)
description: Recupera a marca de inserção atual para a barra de ferramentas.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- controles de Windows de mensagem de TB_GETINSERTMARK
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ee4a51d3110a99013ed26ccb1f2c102e7821873e63dd419b33e92636a1b655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918746"
---
# <a name="tb_getinsertmark-message"></a>TB de \_ mensagem GETINSERTMARK

Recupera a marca de inserção atual para a barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recebe a marca de inserção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB de \_ SETINSERTMARK**](tb-setinsertmark.md)
</dt> </dl>

 

 





