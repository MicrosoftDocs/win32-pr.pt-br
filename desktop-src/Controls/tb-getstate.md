---
title: TB_GETSTATE mensagem (Commctrl.h)
description: Recupera informações sobre o estado do botão especificado em uma barra de ferramentas, como se ele está habilitado, pressionado ou marcado.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1757cfd71427904dc7060cc0084c64b82f143e1a8db666e40fe9e08c64c7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168232"
---
# <a name="tb_getstate-message"></a>Mensagem \_ GETSTATE de TB

Recupera informações sobre o estado do botão especificado em uma barra de ferramentas, como se ele está habilitado, pressionado ou marcado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão para o qual recuperar informações.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará as informações de estado do botão se for bem-sucedido ou -1 caso contrário. As informações de estado do botão podem ser uma combinação dos valores listados em Estados [**do Botão da Barra de Ferramentas**](toolbar-button-states.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





