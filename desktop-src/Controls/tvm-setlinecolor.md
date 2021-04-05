---
title: Mensagem de TVM_SETLINECOLOR (commctrl. h)
description: A \_ mensagem TVM SETLINECOLOR define a cor da linha atual.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Controles de TVM_SETLINECOLOR de mensagens do Windows
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
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009479"
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

## <a name="return-value"></a>Retornar valor

Retorna a cor da linha anterior.

## <a name="remarks"></a>Comentários

Essa mensagem altera apenas as cores de linha. Para alterar as cores de ' + ' e '-' dentro dos botões, use a mensagem [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





