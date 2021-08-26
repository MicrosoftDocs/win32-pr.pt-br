---
title: LVM_SETINSERTMARK mensagem (Commctrl.h)
description: Define o ponto de inserção para a posição definida.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- LVM_SETINSERTMARK controles Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae1cad35bd20605c4cb229dac69eb7461add8b7240b495cc48fb809d39aa098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919856"
---
# <a name="lvm_setinsertmark-message"></a>Mensagem LVM \_ SETINSERTMARK

Define o ponto de inserção para a posição definida.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">estrutura LVINSERTMARK</a> que especifica onde definir o ponto de inserção.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário. **FALSE** será retornado se o tamanho no membro **cbSize** da estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) não for igual ao tamanho real da estrutura ou quando um ponto de inserção não se aplicar na exibição atual.

## <a name="remarks"></a>Comentários

Um ponto de inserção só poderá aparecer se o controle de exibição de lista estiver no modo de exibição de ícone, exibição de ícone pequeno ou exibição deile e não estiver no modo de exibição de grupo.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





