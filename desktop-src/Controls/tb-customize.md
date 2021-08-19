---
title: Mensagem de TB_CUSTOMIZE (commctrl. h)
description: Exibe a caixa de diálogo Personalizar barra de ferramentas.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- controles de Windows de mensagem de TB_CUSTOMIZE
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c4fe1cba535903ff1e60804ee6d4ec5743f5d3726212f9aca16742a40913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957925"
---
# <a name="tb_customize-message"></a>Mensagem de personalização de TB \_

Exibe a caixa de diálogo **Personalizar barra de ferramentas** .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

> [!Note]  
> A barra de ferramentas deve manipular as notificações [tbn \_ QUERYINSERT](tbn-queryinsert.md) e [tbn \_ QUERYDELETE](tbn-querydelete.md) para que a caixa de diálogo **Personalizar barra de ferramentas** seja exibida. Se a barra de ferramentas não tratar essas notificações, a **\_ personalização de TB** não terá nenhum efeito.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





