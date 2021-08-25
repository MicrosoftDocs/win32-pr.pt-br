---
title: Mensagem de LM_SETITEM (commctrl. h)
description: Define os Estados e atributos de um item.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- controles de Windows de mensagem de LM_SETITEM
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dccdb37536352c8783f7dd6af6a9475f5bea69111e2f7f09e5395b0ebf25b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062796"
---
# <a name="lm_setitem-message"></a>\_Mensagem SETITEM de LM

Define os Estados e atributos de um item.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser **NULL**. </dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> que contém os novos Estados e atributos desejados para o link. </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se a mensagem tiver sucesso na definição dos valores e atributos especificados.

## <a name="remarks"></a>Comentários

Com a [**mensagem \_ GETITEM do LM**](lm-getitem.md) , os links só podem ser acessados por meio do índice numérico retornado no membro **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem). Não há suporte para o acesso ao link por meio do nome de ID retornado em **szID** .

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comctl32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





