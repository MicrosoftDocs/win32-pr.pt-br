---
title: Mensagem de TB_GETBUTTONINFO (commctrl. h)
description: Recupera informações estendidas para um botão em uma barra de ferramentas.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- Controles de TB_GETBUTTONINFO de mensagens do Windows
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
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086529"
---
# <a name="tb_getbuttoninfo-message"></a>TB de \_ mensagem GETBUTTONINFO

Recupera informações estendidas para um botão em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que recebe as informações do botão. Os membros **cbSize** e **dwMask** desta estrutura devem ser preenchidos antes do envio desta mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice de base zero do botão ou-1 se ocorrer um erro.

## <a name="remarks"></a>Comentários

Quando você usa caracteres de [**\_ INSERTBUTTON**](tb-insertbutton.md) de [**TB \_**](tb-addbuttons.md) ou TB para posicionar os botões na barra de ferramentas, o texto do botão é normalmente especificado por seu índice de pool de cadeias de caracteres. **TB \_ GETBUTTONINFO** não recuperará essa cadeia de caracteres. Para usar **TB \_ GETBUTTONINFO** para recuperar o texto do botão, você deve primeiro definir a cadeia de texto com [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md). Depois de definir o texto do botão com **TB \_ SETBUTTONINFO**, você não poderá mais usar o índice do pool de cadeias de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) e **TB \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TB de \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB de \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





