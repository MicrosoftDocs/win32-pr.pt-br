---
title: Mensagem de CBEM_SETEXTENDEDSTYLE (commctrl. h)
description: Define os estilos estendidos dentro de um controle ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Controles de CBEM_SETEXTENDEDSTYLE de mensagens do Windows
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
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752946"
---
# <a name="cbem_setextendedstyle-message"></a>\_Mensagem CBEM SETextendedattribute

Define os estilos estendidos dentro de um controle ComboBoxEx.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor **DWORD** que indica quais estilos em *lParam* devem ser afetados. Somente os estilos estendidos em *wParam* serão alterados. Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor **DWORD** que contém os [estilos estendidos do controle ComboBoxEx](comboboxex-control-extended-styles.md) a serem definidos para o controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que contém os estilos estendidos usados anteriormente para o controle.

## <a name="remarks"></a>Comentários

*wParam* permite modificar um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro. Por exemplo, se você passar [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) para *wParam* e 0 para *lParam*, o estilo **CBES \_ ex \_ NOEDITIMAGE** será limpo, mas todos os outros estilos permanecerão os mesmos.

Se você tentar definir um estilo estendido para um controle ComboBoxEx criado com o [**estilo \_ simples do CBS**](combo-box-styles.md) , ele poderá não ser redesenhado corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





