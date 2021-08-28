---
title: Mensagem de RB_MAXIMIZEBAND (commctrl. h)
description: Redimensiona uma faixa em um controle rebar para o tamanho ideal ou maior.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- controles de Windows de mensagem de RB_MAXIMIZEBAND
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
ms.openlocfilehash: 13ef02fbe9611c09d1932907c8218ffd169d3e18d10e0b07faa2b63d50058af1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770086"
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

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





