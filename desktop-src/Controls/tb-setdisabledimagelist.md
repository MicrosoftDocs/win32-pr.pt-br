---
title: TB_SETDISABLEDIMAGELIST mensagem (Commctrl.h)
description: Define a lista de imagens que o controle da barra de ferramentas usará para exibir botões desabilitados.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9125c5e5ac742f4692fc5464cd51c89e111558c4d0004e08d7cef9c862d03cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167486"
---
# <a name="tb_setdisabledimagelist-message"></a>Mensagem TB \_ SETDISABLEDIMAGELIST

Define a lista de imagens que o controle da barra de ferramentas usará para exibir botões desabilitados.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a lista de imagens que será definida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens usada anteriormente para exibir botões desabilitados ou **NULL** se nenhuma lista de imagens foi definida anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





