---
title: CB_SETEXTENDEDUI mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem CB SETEXTENDEDUI para selecionar a interface do usuário padrão ou a interface do usuário estendida para uma caixa de combinação que tem o estilo \_ CBS DROPDOWN ou \_ CBS \_ DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b77e67e555628475b9e40e78b7b0391d0b631fd77e6ff7f549700a553fa507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414218"
---
# <a name="cb_setextendedui-message"></a>Mensagem CB \_ SETEXTENDEDUI

Um aplicativo envia uma mensagem **CB \_ SETEXTENDEDUI** para selecionar a interface do usuário padrão ou a interface do usuário estendida para uma caixa de combinação que tem o estilo [**CBS \_ DROPDOWN**](combo-box-styles.md) ou [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **BOOL** que especifica se a caixa de combinação usa a interface do usuário estendida (**TRUE**) ou a interface do usuário padrão (**FALSE**).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for bem-sucedida, o valor de retorno será CB \_ OK. Se ocorrer um erro, será CB \_ ERR.

## <a name="remarks"></a>Comentários

Por padrão, a tecla F4 abre ou fecha a lista e a seta para baixo altera a seleção atual. Na interface do usuário estendida, a tecla F4 está desabilitada e a tecla SETA PARA BAIXO abre a lista lista listada. A roda do mouse, que normalmente rola pelos itens na lista, não tem efeito quando a interface do usuário estendida é definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Recursos do Combo Box](combo-box-features.md)
</dt> </dl>

 

 





