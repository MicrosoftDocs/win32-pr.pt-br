---
title: Mensagem de TB_SETDRAWTEXTFLAGS (commctrl. h)
description: Define os sinalizadores de desenho de texto para a barra de ferramentas.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Controles de TB_SETDRAWTEXTFLAGS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918858"
---
# <a name="tb_setdrawtextflags-message"></a>TB de \_ mensagem SETDRAWTEXTFLAGS

Define os sinalizadores de desenho de texto para a barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ou mais dos sinalizadores DT \_ , especificados em [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indicam quais bits em *lParam* serão usados ao desenhar o texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ou mais dos sinalizadores DT \_ , especificados em [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indicam como o texto do botão será desenhado. Esse valor será passado para a função **DrawText** quando o texto do botão for desenhado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna os sinalizadores de desenho de texto anteriores.

## <a name="remarks"></a>Comentários

O parâmetro *wParam* permite que você especifique quais sinalizadores serão usados ao desenhar o texto, mesmo se esses sinalizadores estiverem desativados. Por exemplo, se você não quiser que o sinalizador do centro de DT seja \_ usado ao desenhar o texto, você adicionaria o sinalizador do centro de DT \_ a *wParam* e não especificaria o sinalizador do centro de DT \_ em *lParam*. Isso impede que o controle passe o sinalizador do centro de DT \_ para a função [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

