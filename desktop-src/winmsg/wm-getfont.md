---
description: Recupera a fonte com a qual o controle está desenhando seu texto no momento.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Mensagem de WM_GETFONT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790632"
---
# <a name="wm_getfont-message"></a>Mensagem do WM \_ GETfont

Recupera a fonte com a qual o controle está desenhando seu texto no momento.


```C++
#define WM_GETFONT                      0x0031
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

Tipo: **HFONT**

O valor de retorno é um identificador para a fonte usada pelo controle, ou **NULL** se o controle estiver usando a fonte do sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**WM \_ SETfont**](wm-setfont.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 




