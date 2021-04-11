---
title: Mensagem de EM_REPLACESEL (WinUser. h)
description: Substitui o texto selecionado em um controle de edição ou um controle de edição rico pelo texto especificado.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- Controles de EM_REPLACESEL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086419"
---
# <a name="em_replacesel-message"></a>\_Mensagem em REPLACESEL

Substitui o texto selecionado em um controle de edição ou um controle de edição rico pelo texto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se a operação de substituição pode ser desfeita. Se isso for **verdadeiro**, a operação poderá ser desfeita. Se for **false** , a operação não poderá ser desfeita.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o texto de substituição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Use a mensagem em **\_ REPLACESEL** para substituir apenas uma parte do texto em um controle de edição. Para substituir todo o texto, use a mensagem [**\_ SetText do WM**](/windows/desktop/winmsg/wm-settext) .

Se não houver seleção, o texto de substituição será inserido no cursor.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

Em um controle rich edit, o texto de substituição usa a formatação do caractere no cursor ou, se houver uma seleção, do primeiro caractere na seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetText do WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

