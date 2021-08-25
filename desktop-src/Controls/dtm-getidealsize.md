---
title: Mensagem de DTM_GETIDEALSIZE (commctrl. h)
description: Obtém o tamanho necessário para exibir o controle sem recorte. Envie essa mensagem explicitamente ou usando a macro DateTime \_ GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- controles de Windows de mensagem de DTM_GETIDEALSIZE
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
ms.openlocfilehash: 639fbbb25fbf61695f83b54f106f45ff3dd421f528807120be52edd7031e4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878226"
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

## <a name="return-value"></a>Valor retornado

Retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

