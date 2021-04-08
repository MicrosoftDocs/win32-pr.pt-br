---
title: Mensagem de LVM_SETCOLUMNORDERARRAY (commctrl. h)
description: Define a ordem da esquerda para a direita de colunas em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetColumnOrderArray do ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Controles de LVM_SETCOLUMNORDERARRAY de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008859"
---
# <a name="lvm_setcolumnorderarray-message"></a>\_Mensagem SETCOLUMNORDERARRAY LVM

Define a ordem da esquerda para a direita de colunas em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetColumnOrderArray do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamanho, em elementos, do buffer em *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz que especifica a ordem na qual as colunas devem ser exibidas, da esquerda para a direita. Por exemplo, se o conteúdo da matriz for {2,0,1} , o controle exibirá coluna 2, coluna 0 e coluna 1 nessa ordem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





