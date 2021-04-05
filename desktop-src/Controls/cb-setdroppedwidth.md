---
title: Mensagem de CB_SETDROPPEDWIDTH (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETDROPPEDWIDTH para definir a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista \_ suspensa CBS ou CBS \_ .
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- Controles de CB_SETDROPPEDWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824402"
---
# <a name="cb_setdroppedwidth-message"></a>\_Mensagem de SETDROPPEDWIDTH CB

Um aplicativo envia a mensagem **CB \_ SETDROPPEDWIDTH** para definir a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista [**\_ suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A largura mínima permitida da caixa de listagem, em pixels.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for bem-sucedida, o valor de retorno será a nova largura da caixa de listagem.

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

[**\_GETDROPPEDWIDTH CB**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





