---
title: Mensagem de EM_GETMARGINS (WinUser. h)
description: Obtém as larguras das margens esquerda e direita de um controle de edição.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- controles de Windows de mensagem de EM_GETMARGINS
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33746bc44a7b1b0aadd11c573675fedd51e565a557da7601ebe35a4442ddc96c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541066"
---
# <a name="em_getmargins-message"></a>\_Mensagem em GETmargins

Obtém as larguras das margens esquerda e direita de um controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a largura da margem esquerda no LOWORD e a largura da margem direita no HIWORD.

## <a name="remarks"></a>Comentários

**Edição avançada:** Não há suporte para a mensagem em **\_ GetMargins** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETmargins**](em-setmargins.md)
</dt> </dl>

 

 





