---
title: CBEM_GETEDITCONTROL mensagem (Commctrl.h)
description: Obtém o alça para a parte de controle de edição de um controle ComboBoxEx. Um controle ComboBoxEx usa uma caixa de edição quando é definido como o estilo \_ CBS DROPDOWN.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL controles Windows mensagem
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a90a1b37fab7cd8e4a492bd00ad349f96202e13ee25a404f7f4aa41f623e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414066"
---
# <a name="cbem_geteditcontrol-message"></a>Mensagem CBEM \_ GETEDITCONTROL

Obtém o alça para a parte de controle de edição de um controle ComboBoxEx. Um controle ComboBoxEx usa uma caixa de edição quando é definido como o [**estilo \_ CBS DROPDOWN.**](combo-box-styles.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o handle para o controle de edição dentro do controle ComboBoxEx se ele usa o estilo [**\_ CBS DROPDOWN.**](combo-box-styles.md) Caso contrário, a mensagem **retornará NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





