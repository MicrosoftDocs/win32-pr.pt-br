---
title: Mensagem de RB_MAXIMIZEBAND (commctrl. h)
description: Redimensiona uma faixa em um controle rebar para o tamanho ideal ou maior.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- Controles de RB_MAXIMIZEBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824584"
---
# <a name="rb_maximizeband-message"></a>\_Mensagem MAXIMIZEBAND RB

Redimensiona uma faixa em um controle rebar para o tamanho ideal ou maior.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da banda a ser maximizado.

</dd> <dt>

*lParam* 
</dt> <dd>

Indica se a largura ideal da banda deve ser usada quando a banda é maximizada. Se esse valor for diferente de zero, a largura ideal será usada. Se esse valor for zero, a banda será feita o máximo possível.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





