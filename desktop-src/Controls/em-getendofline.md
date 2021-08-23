---
title: EM_GETENDOFLINE mensagem (Commctrl.h)
description: Recupera o caractere de fim de linha usado quando um linebreak é inserido. Envie essa mensagem explicitamente ou usando a macro \_ Editar GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 64ddb55ce592b71c7abaa8c35b1bf14a004b324586094f27a3b418a67e5b24e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019684"
---
# <a name="em_getendofline-message"></a>Mensagem \_ EM GETENDOFLINE

Recupera o caractere de fim de linha para um controle de edição. Envie essa mensagem explicitamente ou usando a [**macro \_ Editar GetEndOfLine.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o caractere de fim de linha usado pelo controle de edição. Esse pode ser um dos valores a seguir.

| Valor                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl> | O caractere de fim de linha usado para novos linebreaks é o retorno de carro seguido por CRLF (linefeed).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | O caractere de fim de linha usado para novos linebreaks é CR (retorno de carro).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | O caractere de fim de linha usado para novos linebreaks é LF (linefeed).<br/>                               |

## <a name="remarks"></a>Comentários

Quando o caractere de fim de linha usado for definido como **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** usando [**Editar \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), essa mensagem retornará o caractere de fim de linha detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10, versão 1809 somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2019 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETENDOFLINE*](em-setendofline.md)
</dt> </dl>
 

 





