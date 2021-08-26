---
title: LVM_INSERTMARKHITTEST mensagem (Commctrl.h)
description: Recupera o ponto de inserção mais próximo de um ponto especificado.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250585fea10846e10238132c5150f5ace9f8e00c474e763023c36c8566fbc752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919976"
---
# <a name="lvm_insertmarkhittest-message"></a>Mensagem LVM \_ INSERTMARKHITTEST

Recupera o ponto de inserção mais próximo de um ponto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Ponteiro para uma **estrutura POINT** que contém as coordenadas de teste de acerto.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">estrutura LVINSERTMARK</a> que especifica o ponto de inserção mais próximo das coordenadas definidas pelo *parâmetro wParam.*</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário. **FALSE** será retornado se o tamanho no membro **cbSize** da estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) não for igual ao tamanho real da estrutura ou quando um ponto de inserção não se aplicar na exibição atual.

## <a name="remarks"></a>Comentários

Um ponto de inserção só poderá aparecer se o controle de exibição de lista estiver no modo de exibição de ícone, exibição de ícone pequeno ou exibição de faixa e não estiver no modo de exibição de grupo.

Se os pontos de inserção não se aplicarem à exibição, a estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) conterá um -1 no **membro iItem.**

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





