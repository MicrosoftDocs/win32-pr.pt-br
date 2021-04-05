---
title: Mensagem de TTM_GETMARGIN (commctrl. h)
description: Recupera as margens superior, esquerda, inferior e direita definidas para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- Controles de TTM_GETMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918470"
---
# <a name="ttm_getmargin-message"></a>Mensagem do TTM \_ GETmargin

Recupera as margens superior, esquerda, inferior e direita definidas para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as informações de margem. Os membros da estrutura **Rect** não definem um retângulo delimitador. Para fins desta mensagem, os membros da estrutura são interpretados da seguinte maneira:



| Valor                                                                                                                                   | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**Início**</dt> </dl>          | Distância entre a borda superior e a parte superior do texto da dica de ferramenta, em pixels.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**mantida**</dt> </dl>       | Distância entre a borda esquerda e a extremidade esquerda do texto da dica de ferramenta, em pixels.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**resultado**</dt> </dl> | Distância entre a borda inferior e a parte inferior do texto da dica de ferramenta, em pixels.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Certo**</dt> </dl>    | Distância entre a borda direita e a extremidade direita do texto da dica de ferramenta, em pixels.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

Todas as quatro margens assumem o padrão de zero quando você cria o controle ToolTip.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TTM \_ SETmargin**](ttm-setmargin.md)
</dt> </dl>

 

