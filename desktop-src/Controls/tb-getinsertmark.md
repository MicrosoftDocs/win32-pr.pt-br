---
title: Mensagem de TB_GETINSERTMARK (commctrl. h)
description: Recupera a marca de inserção atual para a barra de ferramentas.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- Controles de TB_GETINSERTMARK de mensagens do Windows
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
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008992"
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

## <a name="return-value"></a>Retornar valor

Sempre retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB de \_ SETINSERTMARK**](tb-setinsertmark.md)
</dt> </dl>

 

 





