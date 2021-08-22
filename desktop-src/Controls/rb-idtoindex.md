---
title: RB_IDTOINDEX mensagem (Commctrl.h)
description: Converte um identificador de banda em um índice de banda em um controle de barra rebar.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- RB_IDTOINDEX controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b13d243498d821e64be19beebb04fab3f198442aced73ced6f424d32d7177ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642596"
---
# <a name="rb_idtoindex-message"></a>Mensagem \_ RB IDTOINDEX

Converte um identificador de banda em um índice de banda em um controle de barra rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador definido pelo aplicativo da banda em questão. Esse é o valor que foi passado no **membro wID** da [**estrutura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) quando a banda foi inserida.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice de banda baseado em zero se for bem-sucedido ou -1 caso contrário. Se existirem identificadores de banda duplicados, o primeiro será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





