---
title: Mensagem de TB_CUSTOMIZE (commctrl. h)
description: Exibe a caixa de diálogo Personalizar barra de ferramentas.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- Controles de TB_CUSTOMIZE de mensagens do Windows
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
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749069"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

> [!Note]  
> A barra de ferramentas deve manipular as notificações [tbn \_ QUERYINSERT](tbn-queryinsert.md) e [tbn \_ QUERYDELETE](tbn-querydelete.md) para que a caixa de diálogo **Personalizar barra de ferramentas** seja exibida. Se a barra de ferramentas não tratar essas notificações, a **\_ personalização de TB** não terá nenhum efeito.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





