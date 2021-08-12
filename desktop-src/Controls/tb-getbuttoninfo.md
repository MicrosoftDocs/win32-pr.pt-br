---
title: TB_GETBUTTONINFO mensagem (Commctrl.h)
description: Recupera informações estendidas para um botão em uma barra de ferramentas.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 457b8ca82d570b9d6c55cf97392803fce9a81cbe1d5db8122fcdaa975dd99d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669929"
---
# <a name="tb_getbuttoninfo-message"></a>Mensagem \_ GETBUTTONINFO de TB

Recupera informações estendidas para um botão em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que recebe as informações do botão. Os **membros cbSize** **e dwMask** dessa estrutura devem ser preenchidos antes de enviar essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice baseado em zero do botão ou -1 se ocorrer um erro.

## <a name="remarks"></a>Comentários

Quando você usa [**TB \_ ADDBUTTONS**](tb-addbuttons.md) ou [**TB \_ INSERTBUTTON**](tb-insertbutton.md) para colocar botões na barra de ferramentas, o texto do botão geralmente é especificado pelo índice do pool de cadeias de caracteres. **TB \_ GETBUTTONINFO não** recuperará essa cadeia de caracteres. Para usar **TB \_ GETBUTTONINFO para** recuperar o texto do botão, primeiro você deve definir a cadeia de caracteres de texto com TB [**\_ SETBUTTONINFO**](tb-setbuttoninfo.md). Depois de definir o texto do botão com **TB \_ SETBUTTONINFO,** você não poderá mais usar o índice do pool de cadeias de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) e **TB \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





