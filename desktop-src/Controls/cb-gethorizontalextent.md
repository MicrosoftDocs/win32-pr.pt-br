---
title: CB_GETHORIZONTALEXTENT mensagem (Winuser.h)
description: Obtém a largura, em pixels, que a caixa de listagem pode ser rolada horizontalmente (a largura rolável). Isso será aplicável somente se a caixa de listagem tiver uma barra de rolagem horizontal.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- CB_GETHORIZONTALEXTENT controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928561b812dd3a09909d8d89c7dda1dc67b63f9177769d80db2d16ac78cbbf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089206"
---
# <a name="cb_gethorizontalextent-message"></a>Mensagem \_ CB GETHORIZONTALEXTENT

Obtém a largura, em pixels, que a caixa de listagem pode ser rolada horizontalmente (a largura rolável). Isso será aplicável somente se a caixa de listagem tiver uma barra de rolagem horizontal.

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

O valor de retorno é a largura rolável, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CB \_ SETHORIZONTALEXTENT**](cb-sethorizontalextent.md)
</dt> </dl>

 

 





