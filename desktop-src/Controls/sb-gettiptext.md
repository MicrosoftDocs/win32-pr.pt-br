---
title: Mensagem de SB_GETTIPTEXT (commctrl. h)
description: Recupera o texto da dica de ferramenta de uma parte em uma barra de status. A barra de status deve ser criada com o \_ estilo de dicas de ferramenta SBT para habilitar dicas de ferramenta.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- Controles de SB_GETTIPTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824622"
---
# <a name="sb_gettiptext-message"></a>\_Mensagem de GETTIPTEXT SB

Recupera o texto da dica de ferramenta de uma parte em uma barra de status. A barra de status deve ser criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o índice de base zero da parte que recebe o texto da dica de ferramenta. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o tamanho do buffer em *lParam*, em caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer de caracteres que recebe o texto da dica de ferramenta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode causar problemas para seu aplicativo. Por exemplo, se o texto for muito grande para o buffer *lParam* , ele poderá causar um estouro de buffer. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ GETTIPTEXTW** (Unicode) e **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

