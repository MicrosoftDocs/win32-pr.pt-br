---
title: Mensagem de MCM_GETMAXSELCOUNT (commctrl. h)
description: Recupera o intervalo de datas máximo que pode ser selecionado em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Controles de MCM_GETMAXSELCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009522"
---
# <a name="mcm_getmaxselcount-message"></a>\_Mensagem MCM GETMAXSELCOUNT

Recupera o intervalo de datas máximo que pode ser selecionado em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor INT que representa o número total de dias que podem ser selecionados para o controle.

## <a name="remarks"></a>Comentários

Você pode alterar o intervalo de datas máximo que pode ser selecionado usando a mensagem [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





