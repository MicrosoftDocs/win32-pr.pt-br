---
title: Mensagem de TB_GETSTATE (commctrl. h)
description: Recupera informações sobre o estado do botão especificado em uma barra de ferramentas, como se ele está habilitado, pressionado ou marcado.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- Controles de TB_GETSTATE de mensagens do Windows
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
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824245"
---
# <a name="tb_getstate-message"></a>\_Mensagem de SETstate de TB

Recupera informações sobre o estado do botão especificado em uma barra de ferramentas, como se ele está habilitado, pressionado ou marcado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão para o qual recuperar informações.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna as informações de estado do botão se for bem-sucedido ou-1 caso contrário. As informações de estado do botão podem ser uma combinação dos valores listados em [**Estados de botão da barra de ferramentas**](toolbar-button-states.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





