---
title: Mensagem de HDM_SETHOTDIVIDER (commctrl. h)
description: Altera a cor de um divisor entre itens de cabeçalho para indicar o destino de uma operação de arrastar e soltar externa. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetHotDivider do cabeçalho.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- controles de Windows de mensagem de HDM_SETHOTDIVIDER
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedfca7a6f0d10651984efb63c4db63116c4a53d2b9f9b85905c93fc12e6ca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544746"
---
# <a name="hdm_sethotdivider-message"></a>\_Mensagem HDM SETHOTDIVIDER

Altera a cor de um divisor entre itens de cabeçalho para indicar o destino de uma operação de arrastar e soltar externa. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetHotDivider do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de valor representado por *lParam*. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                    | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VERDADEIRO * * * *</dt> </dl>    | Indica que *lParam* mantém as coordenadas do cliente do ponteiro.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Indica que *lParam* contém um valor de índice divisória.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor mantido em *lParam* é interpretado dependendo do valor de *wParam*.

Se *wParam* for **true**, *lParam* representará as coordenadas x e y do ponteiro. A coordenada x está na palavra inferior e a coordenada y está na palavra alta. Quando o controle de cabeçalho recebe a mensagem, ele realça o divisor apropriado com base nas coordenadas *lParam* .

Se *wParam* for **false**, *lParam* representará o índice de inteiro do divisor a ser realçado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor igual ao índice do divisor que o controle realçou.

## <a name="remarks"></a>Comentários

Essa mensagem cria um efeito que um controle de cabeçalho produz automaticamente quando tem o estilo de [**\_ DRAGDROP da HDS**](header-control-styles.md) . A mensagem **HDM \_ SETHOTDIVIDER** é destinada a ser usada quando o proprietário do controle manipula as operações de arrastar e soltar manualmente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





