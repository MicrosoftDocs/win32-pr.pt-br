---
title: Mensagem de EM_SETHYPHENATEINFO (RichEdit. h)
description: Define a maneira como um controle de edição rico faz a hifenização.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Controles de EM_SETHYPHENATEINFO de mensagens do Windows
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
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824686"
---
# <a name="em_sethyphenateinfo-message"></a>\_Mensagem em SETHYPHENATEINFO

Define a maneira como um controle de edição rico faz a hifenização.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma estrutura [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado, deve ser zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> Para habilitar a hifenização, o cliente deve chamar em [**\_ settipografiaoptions**](em-settypographyoptions.md), especificando para \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





