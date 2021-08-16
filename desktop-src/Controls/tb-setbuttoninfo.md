---
title: Mensagem de TB_SETBUTTONINFO (commctrl. h)
description: Define as informações de um botão existente em uma barra de ferramentas.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- controles de Windows de mensagem de TB_SETBUTTONINFO
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

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Normalmente, o texto é atribuído a botões quando eles são adicionados a uma barra de ferramentas especificando o índice de uma cadeia de caracteres no pool de cadeias da barra de ferramentas. Se você usar um **\_ SETBUTTONINFO TB** para atribuir um novo texto a um botão, ele substituirá permanentemente o texto do pool de cadeias de caracteres. Você pode alterar o texto chamando **TB \_ SETBUTTONINFO** novamente, mas não é possível reatribuir a cadeia de caracteres do pool de cadeias de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
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

 

 





