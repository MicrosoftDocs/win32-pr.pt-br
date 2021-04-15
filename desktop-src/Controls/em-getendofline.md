---
title: Mensagem de EM_GETENDOFLINE (commctrl. h)
description: Recupera o caractere de fim de linha usado quando um LineBreak é inserido. Envie essa mensagem explicitamente ou usando a macro Edit \_ GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controles de EM_GETENDOFLINE de mensagens do Windows
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
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454765"
---
# <a name="em_getendofline-message"></a>\_Mensagem em GETENDOFLINE

Recupera o caractere de fim de linha para um controle de edição. Envie essa mensagem explicitamente ou usando a macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o caractere de fim de linha usado pelo controle de edição. Isso pode ser um dos valores a seguir.

| Valor                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**ENDOFLINE da EC \_ \_**</dt> </dl> | O caractere de final de linha usado para o novo quebras é o retorno de carro seguido por linha de alimentação (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | O caractere de final de linha usado para New quebras é retorno de carro (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | O caractere de fim de linha usado para o novo quebras é o LF (alimentação de linhas).<br/>                               |

## <a name="remarks"></a>Comentários

Quando o caractere de final de linha usado é definido como **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** usando [**Editar \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), essa mensagem retornará o caractere de fim de linha detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1809\]<br/>                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETENDOFLINE*](em-setendofline.md)
</dt> </dl>
 

 





