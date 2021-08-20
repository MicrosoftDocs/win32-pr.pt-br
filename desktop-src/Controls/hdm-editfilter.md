---
title: Mensagem de HDM_EDITFILTER (commctrl. h)
description: Move o foco de entrada para a caixa de edição quando um botão de filtro tem o foco.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- controles de Windows de mensagem de HDM_EDITFILTER
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8636c17bfa9043891e5037df79be9c72c1ddc8f3aa2b4d13520f4289205b5099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006156"
---
# <a name="hdm_editfilter-message"></a>\_Mensagem HDM EDITFILTER

Move o foco de entrada para a caixa de edição quando um botão de filtro tem o foco.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor que especifica a coluna a ser editada.

</dd> <dt>

*lParam* 
</dt> <dd>

Um sinalizador que especifica como tratar as alterações de edição do usuário. Use esse sinalizador para especificar o que fazer se o usuário estiver no processo de edição do filtro quando a mensagem for enviada.



| Valor                                                                                                                                      | Significado                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt></dt><dt> **Verdadeiro**</dt> </dl>  | Descarte as alterações feitas pelo usuário. <br/> |
| <dl> <dt></dt><dt> **Falso**</dt> </dl> | Aceite as alterações feitas pelo usuário. <br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um número inteiro. O **LRESULT** é convertido em um inteiro que indica **true**(1) ou **false**(0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HDM \_ CLEARFILTER**](hdm-clearfilter.md)
</dt> </dl>

 

 





