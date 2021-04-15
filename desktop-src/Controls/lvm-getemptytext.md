---
title: Mensagem de LVM_GETEMPTYTEXT (commctrl. h)
description: Obtém o texto destinado à exibição quando o controle de exibição de lista aparece vazio. Envie essa mensagem explicitamente ou usando a \_ macro GetEmptyText do ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Controles de LVM_GETEMPTYTEXT de mensagens do Windows
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
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454630"
---
# <a name="lvm_getemptytext-message"></a>\_Mensagem GETEMPTYTEXT LVM

Obtém o texto destinado à exibição quando o controle de exibição de lista aparece vazio. Envie essa mensagem explicitamente ou usando a macro [**\_ GetEmptyText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O tamanho do buffer apontado por *lParam*, incluindo o **nulo** de terminação.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um buffer Unicode com terminação nula de tamanho especificado por *wParam* para receber o texto. O chamador é responsável por alocar o buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





