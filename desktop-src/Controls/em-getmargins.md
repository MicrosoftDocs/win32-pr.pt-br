---
title: Mensagem de EM_GETMARGINS (WinUser. h)
description: Obtém as larguras das margens esquerda e direita de um controle de edição.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- Controles de EM_GETMARGINS de mensagens do Windows
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
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644349"
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

## <a name="return-value"></a>Retornar valor

Retorna a largura da margem esquerda no LOWORD e a largura da margem direita no HIWORD.

## <a name="remarks"></a>Comentários

**Edição avançada:** Não há suporte para a mensagem em **\_ GetMargins** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_SETmargins**](em-setmargins.md)
</dt> </dl>

 

 





