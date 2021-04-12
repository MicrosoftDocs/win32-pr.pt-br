---
title: Mensagem de SB_SETTIPTEXT (commctrl. h)
description: Define o texto da dica de ferramenta para uma parte em uma barra de status. A barra de status deve ter sido criada com o \_ estilo de dicas de ferramenta SBT para habilitar dicas de ferramenta.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- Controles de SB_SETTIPTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455606"
---
# <a name="sb_settiptext-message"></a>\_Mensagem de SETTIPTEXT SB

Define o texto da dica de ferramenta para uma parte em uma barra de status. A barra de status deve ter sido criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da parte que receberá o texto da dica de ferramenta.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer de caracteres que contém o novo texto de dica de ferramenta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Esse texto de dica de ferramenta é exibido em duas situações:

-   Quando o painel correspondente na barra de status contém apenas um ícone.
-   Quando o painel correspondente na barra de status contém texto truncado devido ao tamanho do painel.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) e **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





