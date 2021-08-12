---
title: Mensagem de TVM_SETLINECOLOR (commctrl. h)
description: A \_ mensagem TVM SETLINECOLOR define a cor da linha atual.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- controles de Windows de mensagem de TVM_SETLINECOLOR
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af66e7a711611ff5e59ec0d68b58a24fb39399245437b0e5d81840c1c38b2d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669516"
---
# <a name="tvm_setlinecolor-message"></a>\_Mensagem TVM SETLINECOLOR

A mensagem **TVM \_ SETLINECOLOR** define a cor da linha atual.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nova cor da linha. Use o \_ valor padrão do CLR para restaurar as cores padrão do sistema.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor da linha anterior.

## <a name="remarks"></a>Comentários

Essa mensagem altera apenas as cores de linha. Para alterar as cores de ' + ' e '-' dentro dos botões, use a mensagem [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





