---
title: Mensagem de LVM_INSERTGROUP (commctrl. h)
description: Insere um grupo em um controle de exibição de lista.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- controles de Windows de mensagem de LVM_INSERTGROUP
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31504226663b0df91e0297ed29abf784ff239dfcee5f323e8617f73dff65acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019244"
---
# <a name="lvm_insertgroup-message"></a>Mensagem de inserção do LVM \_

Insere um grupo em um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Índice em que o grupo deve ser adicionado. Se for-1, o grupo será adicionado ao final da lista.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que contém o grupo a ser adicionado.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do item ao qual o grupo foi adicionado ou-1 se a operação falhou.

## <a name="remarks"></a>Comentários

Para ativar o modo de grupo, chame [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) ou [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).

Um grupo não pode ser inserido em um controle de exibição de lista vazio.

Certifique-se de definir **iGroupId** no (s) item (ns) ao qual o grupo foi adicionado. Caso contrário, após o processamento de mensagens [**\_ ENABLEGROUPVIEW do LVM**](lvm-enablegroupview.md) com **verdadeiro** , o controle ListView não mostrará nenhum item.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32 versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





