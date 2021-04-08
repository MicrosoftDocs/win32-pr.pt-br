---
title: Mensagem de TVM_GETLINECOLOR (commctrl. h)
description: A \_ mensagem TVM GETLINECOLOR Obtém a cor da linha atual.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Controles de TVM_GETLINECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009517"
---
# <a name="tvm_getlinecolor-message"></a>\_Mensagem TVM GETLINECOLOR

A mensagem **TVM \_ GETLINECOLOR** Obtém a cor da linha atual.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a cor da linha atual ou o \_ valor padrão do CLR se nenhum tiver sido especificado.

## <a name="remarks"></a>Comentários

Esta mensagem recupera apenas as cores de linha. Para recuperar as cores de ' + ' e '-' dentro dos botões, use a mensagem [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETLINECOLOR**](tvm-setlinecolor.md)
</dt> </dl>

 

 





