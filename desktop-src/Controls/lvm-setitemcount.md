---
title: Mensagem de LVM_SETITEMCOUNT (commctrl. h)
description: Faz com que o controle de exibição de lista aloque memória para o número especificado de itens ou define o número virtual de itens em um controle de exibição de lista virtual.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- controles de Windows de mensagem de LVM_SETITEMCOUNT
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6b35b38c65663d9811a27341cf10d668a9e045641a8ff0871f6b49fe8bcdbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656276"
---
# <a name="lvm_setitemcount-message"></a>Mensagem do LVM \_ SETitemcount

Faz com que o controle de exibição de lista aloque memória para o número especificado de itens ou define o número virtual de itens em um [controle de exibição de lista virtual](list-view-controls-overview.md).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de itens que o controle de exibição de lista contém, em última instância.

</dd> <dt>

*lParam* 
</dt> <dd>

[Versão 4,70](common-control-versions.md). Valores que especificam o comportamento do controle de exibição de lista depois de redefinir a contagem de itens. Esse valor pode ser uma combinação do seguinte:



| Valor                                                                                                                                                                                    | Significado                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**LVSICF \_ NOINVALIDATEALL**</dt> </dl> | O controle de exibição de lista não será redesenhado a menos que os itens afetados estejam atualmente em exibição.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOscroll**</dt> </dl>                      | O controle de exibição de lista não alterará a posição de rolagem quando a contagem de itens for alterada.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

A forma como a memória é alocada depende de como o controle de exibição de lista foi criado. Você pode enviar essa mensagem explicitamente ou usar as macros de [**ListView \_ setitemcount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) ou [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) . Para obter mais informações, consulte [estilo de List-View virtual](/windows/desktop/Controls/list-view-controls-overview).

Se o controle de exibição de lista tiver sido criado sem o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , o envio dessa mensagem fará com que o controle aloque suas estruturas de dados internas para o número de itens especificado. Isso impede que o controle tenha que alocar as estruturas de dados toda vez que um item é adicionado.

Se o controle de exibição de lista tiver sido criado com o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) (uma exibição de lista virtual), o envio dessa mensagem definirá o número virtual de itens que o controle contém.

O parâmetro *lParam* destina-se somente a controles de exibição de lista que usam os estilos de [**LVS \_ OWNERDATA**](list-view-window-styles.md) e [**LVS \_**](list-view-window-styles.md) de [**\_ lista de LVS**](list-view-window-styles.md) .

Quando a exibição de lista de controle comum é uma exibição de lista virtualizada ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), há um limite de 100 milhões itens na exibição de lista. Nesse cenário, o **LVM \_ setitemcount** retornará false quando tiver um *wParam* de 100.000.001.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

