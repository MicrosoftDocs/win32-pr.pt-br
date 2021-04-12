---
title: Mensagem de EM_SETENDOFLINE (CommCtrl. h)
description: Define o caractere de fim de linha usado quando um LineBreak é inserido.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controles de EM_SETENDOFLINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455764"
---
# <a name="em_setendofline-message"></a>\_Mensagem em SETENDOFLINE

Define o caractere de fim de linha usado quando um LineBreak é inserido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o caractere de fim de linha usado quando um LineBreak é inserido. Isso pode ser um dos valores a seguir.


| Valor                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt> </dl> | Define o caractere de fim de linha usado para New quebras para o caractere usado pelo documento atual.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**ENDOFLINE da EC \_ \_**</dt> </dl>                                        | Define o caractere de fim de linha usado para New quebras para retorno de carro seguido por linha de alimentação (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>                                              | Define o caractere de fim de linha usado para New quebras para retorno de carro (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>                                              | Define o caractere de fim de linha usado para New quebras to avançoing (LF).<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Quando o conjunto de caracteres de fim de linha é o **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, o controle de edição detecta apenas caracteres de fim de linha com suporte de acordo com seu estilo de janela estendido, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 10, 1809\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETENDOFLINE*](em-getendofline.md)
</dt> </dl>

 

 





