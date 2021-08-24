---
title: LVM_GETTILEINFO mensagem (Commctrl.h)
description: Recupera informações sobre um grupo em um controle de exibição de lista.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- LVM_GETTILEINFO controles Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8141b3a39c47966348dfd823b557c1b0af4cca84a90ba979a358d6ac0eaa4757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079030"
---
# <a name="lvm_gettileinfo-message"></a>Mensagem GETTILEINFO do LVM \_

Recupera informações sobre um grupo em um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**estrutura LVTILEINFO**</a> que recebe as informações recuperadas.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

A exibição lado a lado é uma nova maneira de organizar e exibir itens em um controle de exibição de lista. As outras exibições são ícone, ícone pequeno, detalhes e lista.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





