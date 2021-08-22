---
title: TB_ISBUTTONPRESSED mensagem (Commctrl.h)
description: Determina se o botão especificado em uma barra de ferramentas é pressionado.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187b7dd6c39fb972d53391dcbd67d7b45bb895a2e521fa8db22c2a7a411c05e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503636"
---
# <a name="tb_isbuttonpressed-message"></a>Mensagem \_ ISBUTTONPRESSED de TB

Determina se o botão especificado em uma barra de ferramentas é pressionado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se o botão for pressionado ou zero, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





