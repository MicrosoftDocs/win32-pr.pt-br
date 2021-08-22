---
title: LVM_SETCOLUMNORDERARRAY mensagem (Commctrl.h)
description: Define a ordem das colunas da esquerda para a direita em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetColumnOrderArray.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY controles de Windows mensagem
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
ms.openlocfilehash: 9931a7d2c12da02f928c21727292d7d1ce4a430790660afb99ede4bf717c38c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077296"
---
# <a name="lvm_setcolumnorderarray-message"></a>Mensagem LVM \_ SETCOLUMNORDERARRAY

Define a ordem das colunas da esquerda para a direita em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView SetColumnOrderArray.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamanho, em elementos, do buffer em *lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz que especifica a ordem na qual as colunas devem ser exibidas, da esquerda para a direita. Por exemplo, se o conteúdo da matriz for , o controle exibirá a coluna 2, a coluna 0 e a {2,0,1} coluna 1 nessa ordem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





