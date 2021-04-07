---
title: Mensagem de PBM_GETSTATE (commctrl. h)
description: Obtém o estado da barra de progresso.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- Controles de PBM_GETSTATE de mensagens do Windows
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
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918794"
---
# <a name="pbm_getstate-message"></a>\_Mensagem GETstate do PBM

Obtém o estado da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o estado atual da barra de progresso. Um dos valores a seguir.



| Código de retorno                                                                                 | Descrição             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ normal**</dt> </dl> | Em andamento.<br/> |
| <dl> <dt>**erro de PBST \_**</dt> </dl>  | Erro.<br/>       |
| <dl> <dt>**PBST em \_ pausa**</dt> </dl> | Em pausa.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





