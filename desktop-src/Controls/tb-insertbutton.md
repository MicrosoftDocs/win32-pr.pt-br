---
title: Mensagem de TB_INSERTBUTTON (commctrl. h)
description: Insere um botão em uma barra de ferramentas.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- controles de Windows de mensagem de TB_INSERTBUTTON
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909a4e039450e001757cd054cf27a15d24af392d6a55841c2857e2312252145c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829647"
---
# <a name="tb_insertbutton-message"></a>TB de \_ mensagem INSERTBUTTON

Insere um botão em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero de um botão. A mensagem insere o botão novo à esquerda deste botão.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contém informações sobre o botão a ser inserido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ INSERTBUTTONW** (Unicode) e **TB \_ INSERTBUTTONA** (ANSI)<br/>           |



 

 





