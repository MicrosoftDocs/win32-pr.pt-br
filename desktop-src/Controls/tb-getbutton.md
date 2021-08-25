---
title: TB_GETBUTTON mensagem (Commctrl.h)
description: Recupera informações sobre o botão especificado em uma barra de ferramentas.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e36d8cd4e382570884b0cb30f7c95615e2342544cab0970e9864e9fde7882f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919026"
---
# <a name="tb_getbutton-message"></a>Mensagem \_ GETBUTTON de TB

Recupera informações sobre o botão especificado em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero do botão para o qual recuperar informações.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para a [**estrutura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que recebe as informações do botão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





