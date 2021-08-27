---
title: Mensagem de UDM_SETPOS32 (commctrl. h)
description: Define a posição de um controle de cima para baixo com precisão de 32 bits.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- controles de Windows de mensagem de UDM_SETPOS32
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d8dee48c580df72a32bb2072b00cc2dfbdf38b386825d686e8bc8510ba47e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088416"
---
# <a name="udm_setpos32-message"></a>\_Mensagem de SETPOS32 UDM

Define a posição de um controle de cima para baixo com precisão de 32 bits.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Variável do tipo inteiro que especifica a nova posição para o controle acima-abaixo. Se o parâmetro estiver fora do intervalo especificado do controle, *lParam* será definido como o valor válido mais próximo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a posição anterior.

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

[**\_GETPOS32 UDM**](udm-getpos32.md)
</dt> </dl>

 

 





