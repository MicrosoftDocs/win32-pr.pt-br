---
title: LVM_MAPIDTOINDEX mensagem (Commctrl.h)
description: Mapas a ID de um item para um índice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX controles de Windows mensagem
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
ms.openlocfilehash: 77b5380d52f839f28324b808ed0d3304b6c5e2837869e0f0cfc6ab99d8f00b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079866"
---
# <a name="lvm_mapidtoindex-message"></a>Mensagem LVM \_ MAPIDTOINDEX

Mapas a ID de um item para um índice.

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

## <a name="return-value"></a>Valor retornado

Retorna o índice mais atual.

## <a name="remarks"></a>Comentários

Os controles de exibição de lista acompanham internamente os itens por índice. Isso pode apresentar problemas porque os índices podem mudar durante o tempo de vida do controle.

O controle de exibição de lista pode marcar um item com uma ID quando o item é criado. Você pode usar essa ID para garantir a exclusividade durante o tempo de vida do controle de exibição de lista.

Para identificar exclusivamente um item, pegue o índice retornado de uma chamada como [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chame [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md). O valor de retorno é uma ID exclusiva.

Se você precisar do índice de um item após a criação de uma ID, chame **LVM \_ MAPIDTOINDEX** com a ID exclusiva e ele retornará o índice mais atual.

**LVM \_ NÃO há suporte para MAPIDTOINDEX** no estilo [**LVS \_ OWNERDATA.**](list-view-window-styles.md)

> [!Note]  
> Em um ambiente multithread, o índice só é garantido no thread que hospeda o controle de exibição de lista, não em threads em segundo plano.

 

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

