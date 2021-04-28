---
title: Mensagem de TB_GETUNICODEFORMAT (commctrl. h)
description: Mensagem de TB_GETUNICODEFORMAT-recupera o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- Controles de TB_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4beb5a5ff0b71dd76c85db2788d9dc91aa9f4957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106784"
---
# <a name="tb_getunicodeformat-message"></a>TB de \_ mensagem GETUNICODEFORMAT

Recupera o sinalizador de formato de caractere Unicode para o controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**TB de \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)
</dt> </dl>

 

 





