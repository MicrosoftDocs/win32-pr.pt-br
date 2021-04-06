---
title: Mensagem de CBEM_GETEDITCONTROL (commctrl. h)
description: Obtém o identificador para a parte de controle de edição de um controle ComboBoxEx. Um controle ComboBoxEx usa uma caixa de edição quando ela é definida como o \_ estilo DROPDOWN do CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Controles de CBEM_GETEDITCONTROL de mensagens do Windows
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
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086195"
---
# <a name="cbem_geteditcontrol-message"></a>\_Mensagem CBEM GETEDITCONTROL

Obtém o identificador para a parte de controle de edição de um controle ComboBoxEx. Um controle ComboBoxEx usa uma caixa de edição quando ela é definida como o estilo [**\_ DROPDOWN do CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de edição dentro do controle ComboBoxEx se ele usar o estilo [**\_ DROPDOWN do CBS**](combo-box-styles.md) . Caso contrário, a mensagem retornará **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





