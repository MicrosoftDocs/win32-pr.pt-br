---
title: Mensagem de UDM_GETPOS (commctrl. h)
description: Recupera a posição atual de um controle de cima para baixo com precisão de 16 bits.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- controles de Windows de mensagem de UDM_GETPOS
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92ca5fe5d902980560b6879ac7c345230056987308a1e390b0af351281eac62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059776"
---
# <a name="udm_getpos-message"></a>\_Mensagem de GETPOS UDM

Recupera a posição atual de um controle de cima para baixo com precisão de 16 bits.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) será definido como zero e o [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) será definido como a posição atual do controle. Se ocorrer um erro, o **HIWORD** será definido como um valor diferente de zero.

## <a name="remarks"></a>Comentários

Ao processar essa mensagem, o controle de cima para baixo atualiza sua posição atual com base na legenda da janela Buddy. O controle de cima para baixo retornará um erro se não houver nenhuma janela Buddy ou se a legenda especificar um valor inválido ou fora do intervalo. Além disso, um sinalizador de erro é definido no HIWORD do retorno se o controle for criado sem o estilo [**UDS \_ SETBUDDYINT**](up-down-control-styles.md) , embora ele retorne um valor de posição válido no LOWORD do retorno.

Se os valores de 32 bits tiverem sido habilitados para um controle de cima para baixo com o [**UDM \_ SETRANGE32**](udm-setrange32.md), essa mensagem retornará apenas 16 bits inferiores da posição. Para recuperar a posição completa de 32 bits, use o [**UDM \_ GETPOS32**](udm-getpos32.md).

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

[**GetRange do UDM \_**](udm-getrange.md)
</dt> <dt>

[**\_GETRANGE32 UDM**](udm-getrange32.md)
</dt> <dt>

[**\_SETPOS UDM**](udm-setpos.md)
</dt> <dt>

[**\_SETRANGE32 UDM**](udm-setrange32.md)
</dt> </dl>

 

