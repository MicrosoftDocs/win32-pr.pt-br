---
title: SB_GETTIPTEXT mensagem (Commctrl.h)
description: Recupera o texto da dica de ferramenta para uma parte em uma barra de status. A barra de status deve ser criada com o estilo TOOLTIPS do SBT \_ para habilitar dicas de ferramenta.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT controles de Windows mensagem
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
ms.openlocfilehash: 89a78fa6650d850cad2b6de8cc77f1d44b49b8325bf6856b989953fc6511f56f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637126"
---
# <a name="sb_gettiptext-message"></a>Mensagem GETTIPTEXT do SB \_

Recupera o texto da dica de ferramenta para uma parte em uma barra de status. A barra de status deve ser criada com o estilo [**\_ TOOLTIPS do SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o índice baseado em zero da parte que recebe o texto da dica de ferramenta. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o tamanho do buffer em *lParam*, em caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer de caracteres que recebe o texto da dica de ferramenta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode causar problemas para seu aplicativo. Por exemplo, se o texto for muito grande para o buffer *lParam,* ele poderá causar um estouro de buffer. Você deve revisar as [Considerações sobre segurança: Controles Windows Microsoft antes](sec-comctls.md) de continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ GETTIPTEXTW** (Unicode) e **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

