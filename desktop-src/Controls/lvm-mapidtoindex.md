---
title: Mensagem de LVM_MAPIDTOINDEX (commctrl. h)
description: Mapeia a ID de um item para um índice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- Controles de LVM_MAPIDTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748256"
---
# <a name="lvm_mapidtoindex-message"></a>\_Mensagem MAPIDTOINDEX LVM

Mapeia a ID de um item para um índice.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ID exclusiva de um item.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice mais atual.

## <a name="remarks"></a>Comentários

Controles de exibição de lista controlam internamente os itens por índice. Isso pode apresentar problemas porque os índices podem ser alterados durante o tempo de vida do controle.

O controle de exibição de lista pode marcar um item com uma ID quando o item é criado. Você pode usar essa ID para garantir a exclusividade durante o tempo de vida do controle de exibição de lista.

Para identificar exclusivamente um item, pegue o índice que é retornado de uma chamada como [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chame o [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md). O valor de retorno é uma ID exclusiva.

Se você precisar do índice de um item depois que uma ID for criada, poderá chamar o **LVM \_ MAPIDTOINDEX** com a ID exclusiva e ele retornará o índice mais atual.

**LVM \_** Não há suporte para MAPIDTOINDEX no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

> [!Note]  
> Em um ambiente multi-threaded, o índice só é garantido no thread que hospeda o controle de exibição de lista, não em threads em segundo plano.

 

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

