---
title: Mensagem de CCM_SETVERSION (commctrl. h)
description: Essa mensagem é usada para informar o controle de que você está esperando um comportamento associado a uma versão específica.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- Controles de CCM_SETVERSION de mensagens do Windows
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009530"
---
# <a name="ccm_setversion-message"></a>\_Mensagem CCM SETversion

Essa mensagem é usada para informar o controle de que você está esperando um comportamento associado a uma versão específica.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de versão.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a versão especificada na mensagem **CCM \_ SetVersion** anterior. Se *wParam* for definido como um valor maior que a versão atual da dll, ele retornará-1.

## <a name="remarks"></a>Comentários

Em alguns casos, um controle pode se comportar de forma diferente, dependendo da versão. Isso se aplica principalmente a bugs que foram corrigidos em versões posteriores. A mensagem **CCM \_ SetVersion** permite informar ao controle qual comportamento é esperado. Você pode determinar qual versão você especificou enviando uma mensagem [**CCM \_ GetVersion**](ccm-getversion.md) . Para obter um exemplo de como usar essa mensagem, consulte [desenho personalizado com List-View e controles de Tree-View](custom-draw.md).

Se você tiver ComCtl32.dll versão 6 instalada, independentemente do valor que você definiu em *wParam*, a mensagem **CCM \_ SetVersion** retornará a versão 6.

> [!Note]  
> Essa mensagem define apenas o número de versão do controle para o qual ele é enviado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





