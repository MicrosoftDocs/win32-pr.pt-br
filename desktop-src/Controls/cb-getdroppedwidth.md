---
title: Mensagem de CB_GETDROPPEDWIDTH (WinUser. h)
description: Obtém a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista \_ suspensa CBS ou CBS \_ .
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- Controles de CB_GETDROPPEDWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009366"
---
# <a name="cb_getdroppedwidth-message"></a>\_Mensagem de GETDROPPEDWIDTH CB

Obtém a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista [**\_ suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .

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

Se a mensagem tiver sucesso, o valor de retorno será a largura, em pixels.

Se a mensagem falhar, o valor de retorno será CB \_ Err.

## <a name="remarks"></a>Comentários

Por padrão, a largura mínima permitida da caixa de listagem suspensa é zero. A largura da caixa de listagem é a largura mínima permitida ou a largura da caixa de combinação, o que for maior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETDROPPEDWIDTH CB**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





