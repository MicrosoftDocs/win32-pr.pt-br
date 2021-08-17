---
description: enviado a um aplicativo que iniciou um cartão de treinamento com Windows ajuda.
title: Mensagem de WM_TCARD (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85435c5674ad6a2ac4e05edaa5d450dc61de9eac6dae05d3b19662aec91a61f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856981"
---
# <a name="wm_tcard-message"></a>Mensagem do WM \_ TCARD

enviado a um aplicativo que iniciou um cartão de treinamento com Windows ajuda. A mensagem informa ao aplicativo quando o usuário clica em um botão autoria. Um aplicativo inicia um cartão de treinamento especificando o comando HELP \_ TCARD em uma chamada para a função [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idAction* 
</dt> <dd>

Um valor que indica a ação que o usuário executou. Isso pode ser um dos valores a seguir.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

O usuário clicou em um botão de **anulação** autorizada.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**


</dt> <dd>

O usuário clicou em um botão **Cancelar** autorizado.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

O usuário fechou o cartão de treinamento.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

o usuário clicou em um botão de **ajuda** de Windows autorizado.

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

O usuário clicou em um botão **ignorar** autorizado.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**IDOK**


</dt> <dd>

O usuário clicou em um botão **OK** autorizado.

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**IDNO**


</dt> <dd>

O usuário clicou em um botão **não** autorizado.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

O usuário clicou em um botão de **repetição** autoria.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**\_dados de TCARD de ajuda \_**


</dt> <dd>

O usuário clicou em um botão autoria. O parâmetro *dwActionData* contém um inteiro longo especificado pelo autor da ajuda.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**AJUDE a \_ TCARD \_ outro \_ chamador**


</dt> <dd>

Outro aplicativo solicitou cartões de treinamento.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

O usuário clicou em um botão **Sim** autorizado.

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

Se *idAction* especificar \_ o help TCARD \_ data, esse parâmetro será um **longo** especificado pelo autor da ajuda. Caso contrário, esse parâmetro será zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado; Use zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

 




