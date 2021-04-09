---
title: Mensagem de LVM_GETHEADER (commctrl. h)
description: Obtém o identificador para o controle de cabeçalho usado pelo controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetHeader de ListView.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- Controles de LVM_GETHEADER de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008936"
---
# <a name="lvm_getheader-message"></a>Mensagem do LVM \_ GETheader

Obtém o identificador para o controle de cabeçalho usado pelo controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetHeader de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de cabeçalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





