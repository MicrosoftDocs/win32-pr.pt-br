---
title: CQPM_HANDLERSPECIFIC mensagem (Cmnquery.h)
description: Valor base usado para mensagens que são privadas para o manipulador de consulta.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC mensagem do Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd01907a6c5e0e83f9264da56c93b58e56f8b4cb9204f64796af2f7c2b2e788a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021163"
---
# <a name="cqpm_handlerspecific-message"></a>Mensagem CQPM \_ HANDLERSPECIFIC

A **mensagem CQPM \_ HANDLERSPECIFIC** é o valor base usado para mensagens privadas para o manipulador de consulta. O manipulador de consultas deve adicionar esse valor a mensagens privadas para garantir que não ocorram colisões de mensagens.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém dados de mensagem adicionais. O conteúdo desse parâmetro é definido pelo manipulador de consulta.

</dd> <dt>

*lParam* 
</dt> <dd>

Contém dados de mensagem adicionais. O conteúdo desse parâmetro é definido pelo manipulador de consulta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O significado do valor de retorno é definido pelo manipulador de consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Cmnquery.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





