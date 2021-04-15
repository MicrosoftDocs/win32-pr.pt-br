---
title: Mensagem de UDM_GETPOS32 (commctrl. h)
description: Retorna a posição de 32 bits de um controle acima-abaixo.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- Controles de UDM_GETPOS32 de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454816"
---
# <a name="udm_getpos32-message"></a>\_Mensagem de GETPOS32 UDM

Retorna a posição de 32 bits de um controle acima-abaixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um valor **bool** definido como zero se o valor for recuperado com êxito ou diferente de zero se ocorrer um erro. Se esse parâmetro for definido como **NULL**, os erros não serão relatados.

Se o **UDM \_ GETPOS32** for usado em uma situação de processo cruzado, esse parâmetro deverá ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a posição de um controle acima para baixo com precisão de 32 bits. Os aplicativos devem verificar o valor de *lParam* para determinar se o valor de retorno é válido.

## <a name="remarks"></a>Comentários

Quando ele processa essa mensagem, o controle de cima para baixo atualiza sua posição atual com base na legenda da janela Buddy. Ele retornará um erro se não houver nenhuma janela Buddy ou se a legenda especificar um valor inválido ou fora do intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETPOS UDM**](udm-getpos.md)
</dt> <dt>

[**\_SETPOS UDM**](udm-setpos.md)
</dt> <dt>

[**\_SETPOS32 UDM**](udm-setpos32.md)
</dt> </dl>

 

 





