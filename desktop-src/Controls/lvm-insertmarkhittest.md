---
title: Mensagem de LVM_INSERTMARKHITTEST (commctrl. h)
description: Recupera o ponto de inserção mais próximo de um ponto especificado.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- Controles de LVM_INSERTMARKHITTEST de mensagens do Windows
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
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086155"
---
# <a name="lvm_insertmarkhittest-message"></a>\_Mensagem INSERTMARKHITTEST LVM

Recupera o ponto de inserção mais próximo de um ponto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Ponteiro para uma estrutura de **ponto** que contém as coordenadas de teste de clique.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que especifica o ponto de inserção mais próximo das coordenadas definidas pelo parâmetro *wParam* .</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário. **False** será retornado se o tamanho no membro **CbSize** da estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) não for igual ao tamanho real da estrutura ou quando um ponto de inserção não se aplicar na exibição atual.

## <a name="remarks"></a>Comentários

Um ponto de inserção só poderá aparecer se o controle de exibição de lista estiver na exibição de ícones, na exibição de ícones pequenos ou na exibição de bloco e não estiver no modo de exibição de grupo.

Se os pontos de inserção não se aplicarem à exibição, a estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) conterá um-1 no membro **iItem** .

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





