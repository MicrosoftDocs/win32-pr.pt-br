---
title: Mensagem de DM_REPOSITION (WinUser. h)
description: Reposiciona uma caixa de diálogo de nível superior para que ela caiba na área de área de trabalho. Um aplicativo pode enviar essa mensagem a uma caixa de diálogo depois de redimensioná-la para garantir que toda a caixa de diálogo permaneça visível.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Caixas de diálogo de DM_REPOSITION mensagem
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009723"
---
# <a name="dm_reposition-message"></a>\_Mensagem de REposicionamento de DM

Reposiciona uma caixa de diálogo de nível superior para que ela caiba na área de área de trabalho. Um aplicativo pode enviar essa mensagem a uma caixa de diálogo depois de redimensioná-la para garantir que toda a caixa de diálogo permaneça visível.


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Essa mensagem não terá efeito se a caixa de diálogo for uma janela filho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral das caixas de diálogo](dialog-boxes.md)
</dt> </dl>

 

 





