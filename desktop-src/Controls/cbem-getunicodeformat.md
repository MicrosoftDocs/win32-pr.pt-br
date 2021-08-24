---
title: Mensagem de CBEM_GETUNICODEFORMAT (commctrl. h)
description: Obtém o sinalizador de formato de caractere UNICODE para o controle.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- controles de Windows de mensagem de CBEM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4665877c3a9cae9fc559c55040d1972128dbb7404f59e5c61a5739829aca629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699266"
---
# <a name="cbem_getunicodeformat-message"></a>\_Mensagem CBEM GETUNICODEFORMAT

Obtém o sinalizador de formato de caractere UNICODE para o controle.

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

[**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md)
</dt> </dl>

 

 





