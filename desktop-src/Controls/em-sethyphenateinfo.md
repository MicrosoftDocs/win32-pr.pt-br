---
title: EM_SETHYPHENATEINFO mensagem (Richedit.h)
description: Define a maneira como um controle de edição rico faz hifenização.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5551aace3ab054c1c6fa322242ae06386ff19f5a44775bd6dcc6887d19c65c62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437556"
---
# <a name="em_sethyphenateinfo-message"></a>Mensagem EM \_ DOUGYPHENATEINFO

Define a maneira como um controle de edição rico faz hifenização.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma [**estrutura HYPHENATEINFO.**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado, deve ser zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> Para habilitar a hifenização, o cliente deve chamar [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), especificando TO \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





