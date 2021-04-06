---
title: Mensagem de CB_SHOWDROPDOWN (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de lista suspensa CB para mostrar ou ocultar a caixa de listagem de uma caixa de combinação que tem o \_ estilo de lista suspensa CBS ou CBS \_ .
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Controles de CB_SHOWDROPDOWN de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086197"
---
# <a name="cb_showdropdown-message"></a>\_Mensagem de lista suspensa CB

Um aplicativo envia uma mensagem de lista **\_ suspensa CB** para mostrar ou ocultar a caixa de listagem de uma caixa de combinação que tem o estilo de [**\_ lista suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **bool** que especifica se a caixa de listagem suspensa deve ser exibida ou ocultada. Um valor **true** mostra a caixa de listagem; um valor de **false** oculta-o.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é sempre **verdadeiro**.

## <a name="remarks"></a>Comentários

Esta mensagem não tem nenhum efeito em uma caixa de combinação criada com o estilo [**\_ simples do CBS**](combo-box-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CB \_ GETremovestate**](cb-getdroppedstate.md)
</dt> </dl>

 

 





