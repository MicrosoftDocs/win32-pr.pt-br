---
title: Mensagem de TB_GETSTRING (commctrl. h)
description: Recupera uma cadeia de caracteres do pool de cadeias de caracteres de uma barra de ferramentas.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Controles de TB_GETSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009125"
---
# <a name="tb_getstring-message"></a>\_Cadeia de caracteres GETstring de TB

Recupera uma cadeia de caracteres do pool de cadeias de caracteres de uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o comprimento do buffer de *lParam* , em bytes. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o índice da cadeia de caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer usado para retornar a cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o comprimento da cadeia de caracteres se for bem-sucedido ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem retorna a cadeia de caracteres especificada do pool de cadeias de caracteres da barra de ferramentas. Ele não corresponde necessariamente à cadeia de texto que está sendo exibida atualmente por um botão. Para recuperar a cadeia de texto atual de um botão, envie a barra de ferramentas uma mensagem de [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ GETSTRINGW** (Unicode) e **TB \_ getstringa** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_caracteres ADDstring de TB**](tb-addstring.md)
</dt> <dt>

[**hiperbotãos de TB \_**](tb-addbuttons.md)
</dt> <dt>

[**TB de \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

