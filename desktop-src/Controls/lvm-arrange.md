---
title: Mensagem de LVM_ARRANGE (commctrl. h)
description: Organiza os itens na exibição de ícones. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ organização de ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- controles de Windows de mensagem de LVM_ARRANGE
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d7e3595c276815af8708a54d6e81c2a40192d8d07e6cbce514481723799d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062646"
---
# <a name="lvm_arrange-message"></a>Mensagem de organização do LVM \_

Organiza os itens na exibição de ícones. Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ organização de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um dos seguintes valores que especifica o alinhamento:



| Valor                                                                                                                                                            | Significado                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | Não implementado. Em vez disso, aplique o estilo [**LVS \_ ALIGNLEFT**](list-view-window-styles.md) .<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | Não implementado. Em vez disso, aplique o estilo [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**LVA \_ padrão**</dt> </dl>          | Alinha os itens de acordo com os estilos de alinhamento atuais do controle de exibição de lista (o valor padrão).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**LVA \_ SNAPTOGRID**</dt> </dl> | Ajusta todos os ícones para a posição da grade mais próxima.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido; caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





