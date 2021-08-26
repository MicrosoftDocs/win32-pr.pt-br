---
title: LVM_GETINSERTMARK mensagem (Commctrl.h)
description: Recupera a posição do ponto de inserção.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e64281ccc9d4638353ddbb6062ce5cf1c0a678e009639dcc43cd0d4cf52741
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002666"
---
# <a name="lvm_getinsertmark-message"></a>Mensagem \_ GETINSERTMARK LVM

Recupera a posição do ponto de inserção.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">estrutura LVINSERTMARK</a> que recebe a posição do ponto de inserção.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário. **FALSE** será retornado se o tamanho no **membro cbSize** da estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) não for igual ao tamanho real da estrutura.

## <a name="remarks"></a>Comentários

Um ponto de inserção só poderá aparecer se o controle de exibição de lista estiver na exibição de ícones, exibição de ícone pequeno ou exibição deile e não estiver no modo de exibição de grupo.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





