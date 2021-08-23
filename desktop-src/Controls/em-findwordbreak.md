---
title: EM_FINDWORDBREAK mensagem (Richedit.h)
description: Localiza a próxima quebra de palavra antes ou depois da posição de caractere especificada ou recupera informações sobre o caractere nessa posição.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8eaa2a58c8af1181ca22ddd767392749b2c838238e933c52a96268542be0240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541136"
---
# <a name="em_findwordbreak-message"></a>Mensagem EM \_ FINDWORDBREAK

Localiza a próxima quebra de palavra antes ou depois da posição de caractere especificada ou recupera informações sobre o caractere nessa posição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a operação de busca. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**WB \_ CLASSIFY**</dt> </dl>                | Retorna a classe de caracteres e os sinalizadores de quebra de palavras do caractere na posição especificada.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**WB \_ ISDELIMITER**</dt> </dl>       | Retornará **TRUE** se o caractere na posição especificada for um delimiter ou **FALSE** caso contrário.<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB \_ LEFT**</dt> </dl>                            | Localiza o caractere mais próximo antes da posição especificada que inicia uma palavra.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ LEFTBREAK**</dt> </dl>             | Localiza a próxima palavra final antes da posição especificada. Esse valor é o mesmo que \_ PREVBREAK do WB.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB \_ MOVEWORDLEFT**</dt> </dl>    | Localiza o próximo caractere que começa uma palavra antes da posição especificada. Esse valor é usado durante o processamento da tecla CTRL+SETA PARA A ESQUERDA. Esse valor é semelhante a WB \_ MOVEWORDPREV. Consulte Comentários para obter mais informações.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB \_ MOVEWORDRIGHT**</dt> </dl> | Localiza o próximo caractere que começa uma palavra após a posição especificada. Esse valor é usado durante o processamento de tecla CTRL+direita. Esse valor é semelhante a WB \_ MOVEWORDNEXT. Consulte Comentários para obter mais informações.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB \_ RIGHT**</dt> </dl>                         | Localiza o próximo caractere que começa uma palavra após a posição especificada.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB \_ RIGHTBREAK**</dt> </dl>          | Localiza o próximolimidor de fim de palavra após a posição especificada. Esse valor é o mesmo que WB \_ NEXTBREAK.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Posição inicial do caractere baseado em zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A mensagem retorna um valor com base no *parâmetro wParam.*



| Código de retorno                                                                                    | Descrição                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Wparam**</dt> </dl>          | Valor Retornado<br/>                                                                                                |
| <dl> <dt>**WB \_ CLASSIFY**</dt> </dl>    | Retorna a classe de caracteres e os sinalizadores de quebra de palavras do caractere na posição especificada.<br/>                |
| <dl> <dt>**WB \_ ISDELIMITER**</dt> </dl> | Retornará **TRUE** se o caractere na posição especificada for um delimiter; caso contrário, **retornará FALSE.**<br/> |
| <dl> <dt>**Outras pessoas**</dt> </dl>          | Retorna o índice de caracteres da quebra de palavra.<br/>                                                              |



 

## <a name="remarks"></a>Comentários

Se *wParam* for WB LEFT e WB RIGHT, o procedimento de quebra de palavras encontrará quebras de palavras \_ somente após \_ delimitadores. Isso corresponde à funcionalidade de um controle de edição. Se *wParam* for WB \_ MOVEWORDLEFT ou WB MOVEWORDRIGHT, o procedimento de quebra de palavras também comparará classes de caracteres e sinalizadores de quebra \_ de palavras.

Para obter informações sobre classes de caracteres e sinalizadores de quebra de palavras, consulte [Quebras de linha e palavras.](using-rich-edit-controls.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





