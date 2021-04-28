---
title: Mensagem de LVM_SETUNICODEFORMAT (commctrl. h)
description: LVM_SETUNICODEFORMAT mensagem – define o sinalizador de formato de caractere UNICODE para o controle.
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- Controles de LVM_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0f700cd057bc77eddc699404f37b19a6cc9c39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120144"
---
# <a name="lvm_setunicodeformat-message"></a>\_Mensagem SETUNICODEFORMAT LVM

Define o sinalizador de formato de caractere UNICODE para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetUnicodeFormat do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Determina o conjunto de caracteres que é usado pelo controle. Se esse valor for diferente de zero, o controle usará caracteres Unicode. Se esse valor for zero, o controle usará caracteres ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o sinalizador de formato Unicode anterior para o controle.

## <a name="remarks"></a>Comentários

Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_GETUNICODEFORMAT LVM**](lvm-getunicodeformat.md)
</dt> </dl>

 

 





