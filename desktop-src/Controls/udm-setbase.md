---
title: Mensagem de UDM_SETBASE (commctrl. h)
description: Define a base do Radix para um controle de cima para baixo. O valor base determina se a janela buddy exibe números em dígitos decimais ou hexadecimais. Os números hexadecimais são sempre não assinados e números decimais são assinados.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- Controles de UDM_SETBASE de mensagens do Windows
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
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918773"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o valor base anterior. Se uma base inválida for fornecida, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





