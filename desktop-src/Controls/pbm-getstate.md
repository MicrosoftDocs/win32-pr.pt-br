---
title: PBM_GETSTATE mensagem (Commctrl.h)
description: Obtém o estado da barra de progresso.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE controles Windows mensagem
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cd157ccb6ab8a1fe4cd4a31bf1f8a033f0e591288338e21cc322a8ac10bfc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047006"
---
# <a name="pbm_getstate-message"></a>Mensagem \_ GETSTATE do PBM

Obtém o estado da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o estado atual da barra de progresso. Um dos valores a seguir.



| Código de retorno                                                                                 | Descrição             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Em andamento.<br/> |
| <dl> <dt>**ERRO \_ PBST**</dt> </dl>  | Erro.<br/>       |
| <dl> <dt>**PBST \_ PAUSADO**</dt> </dl> | Em pausa.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





