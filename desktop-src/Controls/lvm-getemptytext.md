---
title: LVM_GETEMPTYTEXT mensagem (Commctrl.h)
description: Obtém o texto destinado à exibição quando o controle de exibição de lista aparece vazio. Envie essa mensagem explicitamente ou usando a \_ macro ListView GetEmptyText.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dd1dc1df7b0a558adda37938849b5383bbfee304d807a22a329e4f7301889b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411465"
---
# <a name="lvm_getemptytext-message"></a>Mensagem \_ GETEMPTYTEXT LVM

Obtém o texto destinado à exibição quando o controle de exibição de lista aparece vazio. Envie essa mensagem explicitamente ou usando a [**macro \_ ListView GetEmptyText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

O tamanho do buffer apontado por *lParam*, incluindo o NULL de **terminação.**

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Um ponteiro para um buffer Unicode terminado em nulo de tamanho especificado por *wParam* para receber o texto. O chamador é responsável por alocar o buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





