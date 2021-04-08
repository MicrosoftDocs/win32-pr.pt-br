---
title: Mensagem de UDM_SETPOS (commctrl. h)
description: Define a posição atual para um controle de cima para baixo com precisão de 16 bits.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- Controles de UDM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085916"
---
# <a name="udm_setpos-message"></a>\_Mensagem de SETPOS UDM

Define a posição atual para um controle de cima para baixo com precisão de 16 bits.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nova posição para o controle de cima para baixo. Se o parâmetro estiver fora do intervalo especificado do controle, *lParam* será definido como o valor válido mais próximo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é a posição anterior.

## <a name="remarks"></a>Comentários

Esta mensagem dá suporte apenas a posições de 16 bits. Se os valores de 32 bits tiverem sido habilitados para um controle de cima para baixo com o [**UDM \_ SETRANGE32**](udm-setrange32.md), use o [**UDM \_ SETPOS32**](udm-setpos32.md).

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

[**GetRange do UDM \_**](udm-getrange.md)
</dt> <dt>

[**\_GETPOS UDM**](udm-getpos.md)
</dt> </dl>

 

 





