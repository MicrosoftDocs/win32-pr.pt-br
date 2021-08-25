---
title: TB_ISBUTTONHIGHLIGHTED mensagem (Commctrl.h)
description: Verifica o estado de realça de um botão de barra de ferramentas.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- TB_ISBUTTONHIGHLIGHTED controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903932fddb7bf356a89adda0513a045d099a22c459add6401818eec54a3f0657
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918366"
---
# <a name="tb_isbuttonhighlighted-message"></a>Mensagem \_ ISBUTTONHIGHLIGHTED de TB

Verifica o estado de realça de um botão de barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando para um botão de barra de ferramentas.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se o botão estiver realçado ou zero, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





