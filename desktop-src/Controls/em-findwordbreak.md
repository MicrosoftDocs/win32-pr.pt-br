---
title: Mensagem de EM_FINDWORDBREAK (RichEdit. h)
description: Localiza a próxima quebra de palavra antes ou depois da posição do caractere especificado ou recupera informações sobre o caractere nessa posição.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- Controles de EM_FINDWORDBREAK de mensagens do Windows
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
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455281"
---
# <a name="em_findwordbreak-message"></a>\_Mensagem em FINDWORDBREAK

Localiza a próxima quebra de palavra antes ou depois da posição do caractere especificado ou recupera informações sobre o caractere nessa posição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a operação Localizar. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**WB \_ classificar**</dt> </dl>                | Retorna os sinalizadores de classe de caractere e de quebra de palavra do caractere na posição especificada.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**\_delimitador WB**</dt> </dl>       | Retornará **true** se o caractere na posição especificada for um delimitador ou **false** caso contrário.<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB \_ à esquerda**</dt> </dl>                            | Localiza o caractere mais próximo antes da posição especificada que inicia uma palavra.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ LEFTBREAK**</dt> </dl>             | Localiza a próxima palavra final antes da posição especificada. Esse valor é o mesmo que WB \_ PREVBREAK.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB \_ MOVEWORDLEFT**</dt> </dl>    | Localiza o próximo caractere que inicia uma palavra antes da posição especificada. Esse valor é usado durante o processamento da tecla CTRL + seta para a esquerda. Esse valor é semelhante a WB \_ MOVEWORDPREV. Consulte comentários para obter mais informações.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB \_ MOVEWORDRIGHT**</dt> </dl> | Localiza o próximo caractere que inicia uma palavra após a posição especificada. Esse valor é usado durante o processamento da tecla CTRL + direita. Esse valor é semelhante a WB \_ MOVEWORDNEXT. Consulte comentários para obter mais informações.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB \_ à direita**</dt> </dl>                         | Localiza o próximo caractere que inicia uma palavra após a posição especificada.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB \_ RIGHTBREAK**</dt> </dl>          | Localiza o próximo delimitador de fim de palavra após a posição especificada. Esse valor é o mesmo que WB \_ NEXTBREAK.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Posição inicial de caracteres com base em zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A mensagem retorna um valor com base no parâmetro *wParam* .



| Código de retorno                                                                                    | Descrição                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**wParam**</dt> </dl>          | Valor Retornado<br/>                                                                                                |
| <dl> <dt>**WB \_ classificar**</dt> </dl>    | Retorna os sinalizadores de classe de caractere e de quebra de palavra do caractere na posição especificada.<br/>                |
| <dl> <dt>**\_delimitador WB**</dt> </dl> | Retornará **true** se o caractere na posição especificada for um delimitador; caso contrário, retornará **false**.<br/> |
| <dl> <dt>**Outros**</dt> </dl>          | Retorna o índice de caracteres da quebra de palavra.<br/>                                                              |



 

## <a name="remarks"></a>Comentários

Se *wParam* for WB \_ Left e WB \_ Right, o procedimento de quebra de palavra localizará quebras de palavras somente após os delimitadores. Isso corresponde à funcionalidade de um controle de edição. Se *wParam* for WB \_ MOVEWORDLEFT ou WB \_ MOVEWORDRIGHT, o procedimento de quebra de palavra também comparará classes de caracteres e sinalizadores de quebra de palavras.

Para obter informações sobre classes de caracteres e sinalizadores de quebra de palavras, consulte [quebras de linha e de palavras](using-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





