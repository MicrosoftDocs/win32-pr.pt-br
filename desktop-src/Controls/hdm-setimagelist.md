---
title: Mensagem de HDM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetImageList ou header \_ SetStateImageList do cabeçalho.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Controles de HDM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918390"
---
# <a name="hdm_setimagelist-message"></a>\_Mensagem HDM SETimagelist

Atribui uma lista de imagens a um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) ou [**header \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) do cabeçalho.

## <a name="parameters"></a>Parâmetros

<dl> <dt>*wParam*</dt> <dd>Um dos seguintes valores:

| Valor                                                                                                                                                      | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normal**</dt> </dl> | Indica que esta é uma lista de imagens normal.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**\_estado HDSIL**</dt> </dl>    | Indica que esta é uma lista de imagens de estado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para uma lista de imagens.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens associada anteriormente ao controle. Retorna **NULL** após a falha ou se nenhuma lista de imagens foi definida anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





