---
title: Mensagem de HDM_EDITFILTER (commctrl. h)
description: Move o foco de entrada para a caixa de edição quando um botão de filtro tem o foco.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- Controles de HDM_EDITFILTER de mensagens do Windows
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
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644845"
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

## <a name="return-value"></a>Retornar valor

Retorna um número inteiro. O **LRESULT** é convertido em um inteiro que indica **true**(1) ou **false**(0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**HDM \_ CLEARFILTER**](hdm-clearfilter.md)
</dt> </dl>

 

 





