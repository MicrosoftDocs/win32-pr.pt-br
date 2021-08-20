---
title: TB_SETBUTTONINFO mensagem (Commctrl.h)
description: Define as informações de um botão existente em uma barra de ferramentas.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fa1da0f9556c025b83ac2b3345680fe11dac0dd15e202ed7336cacfe511e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829620"
---
# <a name="tb_setbuttoninfo-message"></a>Mensagem \_ TB SETBUTTONINFO

Define as informações de um botão existente em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de botão.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que contém as novas informações de botão. Os **membros cbSize** **e dwMask** dessa estrutura devem ser preenchidos antes de enviar essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="remarks"></a>Comentários

O texto é normalmente atribuído aos botões quando eles são adicionados a uma barra de ferramentas especificando o índice de uma cadeia de caracteres no pool de cadeias de caracteres da barra de ferramentas. Se você usar um **TB \_ SETBUTTONINFO** para atribuir um novo texto a um botão, ele substituirá permanentemente o texto do pool de cadeias de caracteres. Você pode alterar o texto chamando **TB \_ SETBUTTONINFO** novamente, mas não pode reatribuir a cadeia de caracteres do pool de cadeias de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ SETBUTTONINFOW** (Unicode) e **TB \_ SETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_ADDBUTTONS DE TB**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





