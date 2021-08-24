---
title: Mensagem de SB_SETTIPTEXT (commctrl. h)
description: Define o texto da dica de ferramenta para uma parte em uma barra de status. A barra de status deve ter sido criada com o \_ estilo de dicas de ferramenta SBT para habilitar dicas de ferramenta.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- controles de Windows de mensagem de SB_SETTIPTEXT
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
ms.openlocfilehash: 864ba53066b000f9f7ae65365341238a701b4e70bc4ce8cc70adba923d57a5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637016"
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

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Esse texto de dica de ferramenta é exibido em duas situações:

-   Quando o painel correspondente na barra de status contém apenas um ícone.
-   Quando o painel correspondente na barra de status contém texto truncado devido ao tamanho do painel.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) e **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





