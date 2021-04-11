---
description: Um aplicativo envia a mensagem do WM \_ MDITILE para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas MDI em um formato de bloco.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Mensagem de WM_MDITILE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164421"
---
# <a name="wm_mditile-message"></a>Mensagem do WM \_ MDITILE

Um aplicativo envia a mensagem do **WM \_ MDITILE** para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas MDI em um formato de bloco.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A opção de divisão. Esse parâmetro pode ser um dos valores a seguir, opcionalmente combinado com **MDITILE \_ SKIPDISABLED** para impedir que janelas filho MDI desabilitadas sejam colocadas lado a lado.



| Valor                                                                                                                                                                                                                                    | Significado                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0001</dt> horizontal </dl> | Janelas de blocos horizontalmente.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0000</dt> vertical </dl>       | Janelas de blocos verticalmente.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **bool**

Se a mensagem tiver sucesso, o valor de retorno será **true**.

Se a mensagem falhar, o valor de retorno será **false**.

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

[**MDICASCADE do WM \_**](wm-mdicascade.md)
</dt> <dt>

[**MDIICONARRANGE do WM \_**](wm-mdiiconarrange.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




