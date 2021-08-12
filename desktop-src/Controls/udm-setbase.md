---
title: Mensagem de UDM_SETBASE (commctrl. h)
description: Define a base do Radix para um controle de cima para baixo. O valor base determina se a janela buddy exibe números em dígitos decimais ou hexadecimais. Os números hexadecimais são sempre não assinados e números decimais são assinados.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- controles de Windows de mensagem de UDM_SETBASE
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f9fd3750a70e676c3e9f32efe9ff0bfd9b300b812d09f4a04c34e4a90f36933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669074"
---
# <a name="udm_setbase-message"></a>Mensagem do UDM \_ SETbase

Define a base do Radix para um controle de cima para baixo. O valor base determina se a janela buddy exibe números em dígitos decimais ou hexadecimais. Os números hexadecimais são sempre não assinados e números decimais são assinados.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Novo valor base para o controle. Esse parâmetro pode ser 10 para decimal ou 16 para hexadecimal.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o valor base anterior. Se uma base inválida for fornecida, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





