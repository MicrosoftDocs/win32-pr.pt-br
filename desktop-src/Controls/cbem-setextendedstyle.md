---
title: CBEM_SETEXTENDEDSTYLE mensagem (Commctrl.h)
description: Define estilos estendidos em um controle ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE controles de Windows mensagem
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd1083e838d85f9cb659acb9a28b74a1d8605934be4c53fd72993e7470fad2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527966"
---
# <a name="cbem_setextendedstyle-message"></a>Mensagem CBEM \_ SETEXTENDEDSTYLE

Define estilos estendidos em um controle ComboBoxEx.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **valor DWORD** que indica quais estilos em *lParam* devem ser afetados. Somente os estilos estendidos *no wParam* serão alterados. Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.

</dd> <dt>

*lParam* 
</dt> <dd>

Um **valor DWORD** que contém os Estilos Estendidos [do Controle ComboBoxEx](comboboxex-control-extended-styles.md) a ser definido para o controle.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor DWORD** que contém os estilos estendidos usados anteriormente para o controle .

## <a name="remarks"></a>Comentários

*O wParam* permite que você modifique um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro. Por exemplo, se você passar [**CBES \_ EX \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) para *wParam* e 0 para *lParam*, o estilo **CBES \_ EX \_ NOEDITIMAGE** será limpo, mas todos os outros estilos permanecerão os mesmos.

Se você tentar definir um estilo estendido para um controle ComboBoxEx criado com o estilo [**CBS \_ SIMPLE,**](combo-box-styles.md) ele poderá não reintint corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





