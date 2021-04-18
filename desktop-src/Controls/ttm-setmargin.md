---
title: Mensagem de TTM_SETMARGIN (commctrl. h)
description: Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- Controles de TTM_SETMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751300"
---
# <a name="ttm_setmargin-message"></a>\_Mensagem TTM SETmargin

Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as informações de margem a serem definidas. Os membros da estrutura **Rect** não definem um retângulo delimitador. Para fins desta mensagem, os membros da estrutura são interpretados da seguinte maneira:



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

Esta mensagem não tem efeito quando o aplicativo é executado no Windows Vista e os estilos visuais estão habilitados para a dica de ferramenta. Você pode desabilitar estilos visuais para a dica de ferramenta usando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetMargin TTM \_**](ttm-getmargin.md)
</dt> </dl>

 

