---
title: Mensagem de TB_GETOBJECT (commctrl. h)
description: Recupera o IDropTarget para um controle ToolBar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Controles de TB_GETOBJECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086014"
---
# <a name="tb_getobject-message"></a>\_Mensagem de objeto GETobject de TB

Recupera o [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para um controle ToolBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador da interface que está sendo solicitada. Esse valor deve apontar para **\_ IDropTarget IID**.

</dd> <dt>

*lParam* 
</dt> <dd>

Endereço que recebe o ponteiro de interface. Se ocorrer um erro, um ponteiro **NULL** será colocado nesse endereço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que indica êxito ou falha da operação.

## <a name="remarks"></a>Comentários

A [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) da barra de ferramentas é usada pela barra de ferramentas quando os objetos são arrastados ou soltos nela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

