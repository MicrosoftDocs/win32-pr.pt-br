---
title: Mensagem de LVM_GETUNICODEFORMAT (commctrl. h)
description: Recupera o sinalizador de formato de caractere UNICODE para o controle. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetUnicodeFormat do ListView.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- Controles de LVM_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824666"
---
# <a name="lvm_getunicodeformat-message"></a>\_Mensagem GETUNICODEFORMAT LVM

Recupera o sinalizador de formato de caractere UNICODE para o controle. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetUnicodeFormat do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o sinalizador de formato Unicode para o controle. Se esse valor for diferente de zero, o controle estará usando caracteres Unicode. Se esse valor for zero, o controle estará usando caracteres ANSI.

## <a name="remarks"></a>Comentários

Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_SETUNICODEFORMAT LVM**](lvm-setunicodeformat.md)
</dt> </dl>

 

 





