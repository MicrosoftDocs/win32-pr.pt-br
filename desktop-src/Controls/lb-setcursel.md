---
title: Mensagem de LB_SETCURSEL (WinUser. h)
description: Seleciona uma cadeia de caracteres e a rola para a exibição, se necessário. Quando a nova cadeia de caracteres é selecionada, a caixa de listagem remove o realce da cadeia de caracteres selecionada anteriormente.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- Controles de LB_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751151"
---
# <a name="lb_setcursel-message"></a>\_Mensagem de DEcursão de lb

Seleciona uma cadeia de caracteres e a rola para a exibição, se necessário. Quando a nova cadeia de caracteres é selecionada, a caixa de listagem remove o realce da cadeia de caracteres selecionada anteriormente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero da cadeia de caracteres selecionada. Se esse parâmetro for-1, a caixa de listagem será definida como sem seleção.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será um erro de LB \_ . Se o parâmetro *wParam* for-1, o valor de retorno será de \_ erro lb mesmo que nenhum erro tenha ocorrido.

## <a name="remarks"></a>Comentários

Use essa mensagem somente com caixas de listagem de seleção única. Você não pode usá-lo para definir ou remover uma seleção em uma caixa de listagem de seleção múltipla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**KG \_ de lb**](lb-getcursel.md)
</dt> </dl>

 

 





