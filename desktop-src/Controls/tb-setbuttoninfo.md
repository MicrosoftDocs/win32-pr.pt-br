---
title: Mensagem de TB_SETBUTTONINFO (commctrl. h)
description: Define as informações de um botão existente em uma barra de ferramentas.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- Controles de TB_SETBUTTONINFO de mensagens do Windows
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
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824753"
---
# <a name="tb_setbuttoninfo-message"></a>TB de \_ mensagem SETBUTTONINFO

Define as informações de um botão existente em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de botão.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que contém as informações do novo botão. Os membros **cbSize** e **dwMask** desta estrutura devem ser preenchidos antes do envio desta mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Normalmente, o texto é atribuído a botões quando eles são adicionados a uma barra de ferramentas especificando o índice de uma cadeia de caracteres no pool de cadeias da barra de ferramentas. Se você usar um **\_ SETBUTTONINFO TB** para atribuir um novo texto a um botão, ele substituirá permanentemente o texto do pool de cadeias de caracteres. Você pode alterar o texto chamando **TB \_ SETBUTTONINFO** novamente, mas não é possível reatribuir a cadeia de caracteres do pool de cadeias de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ SETBUTTONINFOW** (Unicode) e **TB \_ SETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**hiperbotãos de TB \_**](tb-addbuttons.md)
</dt> <dt>

[**TB de \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB de \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> <dt>

[**TB \_ GETstring**](tb-getstring.md)
</dt> <dt>

[**TB de \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





