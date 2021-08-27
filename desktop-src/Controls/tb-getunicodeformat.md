---
title: Mensagem de TB_GETUNICODEFORMAT (commctrl. h)
description: Mensagem de TB_GETUNICODEFORMAT-recupera o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- controles de Windows de mensagem de TB_GETUNICODEFORMAT
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
ms.openlocfilehash: aa59269813dde63f15980abc919e50cfaf4dcf5a3c86da311f2aa5206618e88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061365"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB de \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)
</dt> </dl>

 

 





