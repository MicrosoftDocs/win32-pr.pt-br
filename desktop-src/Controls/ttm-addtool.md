---
title: Mensagem de TTM_ADDTOOL (commctrl. h)
description: Registra uma ferramenta com um controle ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- controles de Windows de mensagem de TTM_ADDTOOL
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb66c43033e54ce51b396ff5bb11efe3b2a99e8eb2578a2e9fe4d4bc4487ccf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769536"
---
# <a name="ttm_addtool-message"></a>\_Mensagem ADDFERRAMENTA TTM

Registra uma ferramenta com um controle ToolTip.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que contém informações que o controle ToolTip precisa para exibir o texto da ferramenta. O membro **cbSize** dessa estrutura deve ser preenchido antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ ADDTOOLW** (Unicode) e **TTM \_ addferramentaa** (ANSI)<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TTM \_ DELTOOL**](ttm-deltool.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre os controles de dica de ferramenta](tooltip-controls.md)
</dt> </dl>

 

 





