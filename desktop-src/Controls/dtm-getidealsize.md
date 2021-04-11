---
title: Mensagem de DTM_GETIDEALSIZE (commctrl. h)
description: Obtém o tamanho necessário para exibir o controle sem recorte. Envie essa mensagem explicitamente ou usando a macro DateTime \_ GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Controles de DTM_GETIDEALSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163585"
---
# <a name="dtm_getidealsize-message"></a>\_Mensagem DTM GETIDEALSIZE

Obtém o tamanho necessário para exibir o controle sem recorte. Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado. Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) para receber o tamanho ideal. O aplicativo de chamada é responsável por alocar essa estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

