---
title: TTM_SETMARGIN mensagem (Commctrl.h)
description: Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN controles Windows mensagem
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
ms.openlocfilehash: 04e5792b33f7f9f5a997759ba390c1b8a713308f95c4ba3f7b5cd0460747ff62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914056"
---
# <a name="ttm_setmargin-message"></a>Mensagem TTM \_ SETMARGIN

Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que contém as informações de margem a serem definidas. Os membros da estrutura **RECT** não definem um retângulo delimitar. Para a finalidade desta mensagem, os membros da estrutura são interpretados da seguinte maneira:



| Valor                                                                                                                                   | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**Início**</dt> </dl>          | Distância entre a borda superior e a parte superior do texto da dica de ferramenta, em pixels.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**Deixou**</dt> </dl>       | Distância entre a borda esquerda e a extremidade esquerda do texto da dica de ferramenta, em pixels.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**Fundo**</dt> </dl> | Distância entre a borda inferior e a parte inferior do texto da dica de ferramenta, em pixels.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Certo**</dt> </dl>    | Distância entre a borda direita e a extremidade direita do texto da dica de ferramenta, em pixels.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="remarks"></a>Comentários

Essa mensagem não tem efeito quando o aplicativo é executado Windows vista e estilos visuais estão habilitados para a dica de ferramenta. Você pode desabilitar estilos visuais para a dica de ferramenta [**usando SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TTM \_ GETMARGIN**](ttm-getmargin.md)
</dt> </dl>

 

