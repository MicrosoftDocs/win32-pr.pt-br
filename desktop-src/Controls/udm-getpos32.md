---
title: Mensagem de UDM_GETPOS32 (commctrl. h)
description: Retorna a posição de 32 bits de um controle acima-abaixo.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- controles de Windows de mensagem de UDM_GETPOS32
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
ms.openlocfilehash: a11d043ca4f6b69a554b43d5abeaf35e4c2a2a6d72797e829900529df70b6c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059786"
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

## <a name="return-value"></a>Valor retornado

Retorna a posição de um controle acima para baixo com precisão de 32 bits. Os aplicativos devem verificar o valor de *lParam* para determinar se o valor de retorno é válido.

## <a name="remarks"></a>Comentários

Quando ele processa essa mensagem, o controle de cima para baixo atualiza sua posição atual com base na legenda da janela Buddy. Ele retornará um erro se não houver nenhuma janela Buddy ou se a legenda especificar um valor inválido ou fora do intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



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

 

 





