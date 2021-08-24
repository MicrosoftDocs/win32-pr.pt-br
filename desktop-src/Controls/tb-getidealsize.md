---
title: TB_GETIDEALSIZE mensagem (Commctrl.h)
description: Obtém o tamanho ideal da barra de ferramentas.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1844f3ae4200c1120f784c03e5f80d2df4457319cf81e12c88ce0ed84525117d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816306"
---
# <a name="tb_getidealsize-message"></a>Mensagem \_ GETIDEALSIZE de TB

Obtém o tamanho ideal da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Um **BOOL** que indica se a altura ideal ou a largura da barra de ferramentas deve ser recuperada. Use **TRUE** para recuperar a altura ideal, **FALSE** para recuperar a largura ideal.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura SIZE**](/previous-versions//dd145106(v=vs.85)) que recebe a altura ou a largura na qual todos os botões seriam exibidos. Se *wParam* for **TRUE,** somente o **membro cy** (altura) será válido. Se *wParam* for **FALSE,** somente o **membro cx** (largura) será válido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

