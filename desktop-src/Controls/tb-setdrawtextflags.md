---
title: TB_SETDRAWTEXTFLAGS mensagem (Commctrl.h)
description: Define os sinalizadores de desenho de texto para a barra de ferramentas.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS controles de Windows mensagem
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
ms.openlocfilehash: 849bbb0e661c9e8afe246894d2d2f59d99d15a3f096ad2295a7018cf3df26ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543876"
---
# <a name="tb_setdrawtextflags-message"></a>Mensagem TB \_ SETDRAWTEXTFLAGS

Define os sinalizadores de desenho de texto para a barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ou mais dos sinalizadores DT, especificados em DrawText , que indicam quais bits em \_ *lParam* serão usados ao desenhar o texto. [](/windows/desktop/api/winuser/nf-winuser-drawtext)

</dd> <dt>

*lParam* 
</dt> <dd>

Um ou mais sinalizadores \_ DT, especificados em [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indicam como o texto do botão será desenhado. Esse valor será passado para a **função DrawText** quando o texto do botão for desenhado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna os sinalizadores de desenho de texto anteriores.

## <a name="remarks"></a>Comentários

O *parâmetro wParam* permite que você especifique quais sinalizadores serão usados ao desenhar o texto, mesmo que esses sinalizadores sejam desligados. Por exemplo, se você não quiser que o sinalizador DT CENTER seja usado ao desenhar texto, adicione o sinalizador DT CENTER ao wParam e não especifique o sinalizador \_ \_ DT CENTER em  \_ *lParam*. Isso impede que o controle passe o sinalizador DT \_ CENTER para a função [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

