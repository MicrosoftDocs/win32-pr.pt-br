---
title: CCM_SETVERSION mensagem (Commctrl.h)
description: Essa mensagem é usada para informar o controle de que você está esperando um comportamento associado a uma versão específica.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION controles Windows mensagem
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
ms.openlocfilehash: b9453b99ff9cd23675b3b5d79593071e4ebb3fbb65d06a78d0fe8094154b2486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320096"
---
# <a name="ccm_setversion-message"></a>Mensagem \_ SETVERSION do CCM

Essa mensagem é usada para informar o controle de que você está esperando um comportamento associado a uma versão específica.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de versão.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a versão especificada na mensagem **\_ SETVERSION do CCM** anterior. Se *wParam* for definido como um valor maior que a versão da DLL atual, ele retornará -1.

## <a name="remarks"></a>Comentários

Em alguns casos, um controle pode se comportar de maneira diferente, dependendo da versão. Isso se aplica principalmente a bugs que foram corrigidos em versões posteriores. A **mensagem \_ SETVERSION do CCM** permite que você informe ao controle qual comportamento é esperado. Você pode determinar qual versão você especificou enviando uma mensagem [**\_ GETVERSION do CCM.**](ccm-getversion.md) Para ver um exemplo de como usar essa mensagem, consulte [Custom Draw With List-View and Tree-View Controls](custom-draw.md).

Se você tiver ComCtl32.dll versão 6 instalada, independentemente do valor definido em *wParam*, a mensagem **\_ SETVERSION** do CCM retornará a versão 6.

> [!Note]  
> Essa mensagem define apenas o número de versão para o controle ao qual ela é enviada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





