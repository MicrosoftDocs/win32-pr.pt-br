---
title: Mensagem de EM_SETENDOFLINE (CommCtrl. h)
description: Define o caractere de fim de linha usado quando um LineBreak é inserido.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- controles de Windows de mensagem de EM_SETENDOFLINE
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
ms.openlocfilehash: 5990b247757fc8e3cd39ab38edf5b88ca8ac62f74e402aac3899d51e3156231f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437586"
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

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com sucesso, o valor de retorno será diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Quando o conjunto de caracteres de fim de linha é o **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, o controle de edição detecta apenas caracteres de fim de linha com suporte de acordo com seu estilo de janela estendido, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, 1809 \[ aplicativos de área de trabalho apenas\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2019\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETENDOFLINE*](em-getendofline.md)
</dt> </dl>

 

 





