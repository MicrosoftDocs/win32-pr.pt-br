---
title: Mensagem de CQPM_HANDLERSPECIFIC (Cmnquery. h)
description: Valor base usado para mensagens que são privadas para o manipulador de consulta.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_HANDLERSPECIFIC Active Directory
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
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454769"
---
# <a name="cqpm_handlerspecific-message"></a>\_Mensagem CQPM HANDLERSPECIFIC

A mensagem **CQPM \_ HANDLERSPECIFIC** é o valor base usado para mensagens que são particulares ao manipulador de consultas. O manipulador de consulta deve adicionar esse valor a mensagens privadas para garantir que as colisões de mensagem não ocorram.

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

## <a name="return-value"></a>Retornar valor

O significado do valor de retorno é definido pelo manipulador de consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





