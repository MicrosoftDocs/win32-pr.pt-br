---
description: Um aplicativo envia a mensagem do WM \_ MDICASCADE para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas em um formato em cascata.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Mensagem de WM_MDICASCADE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296289"
---
# <a name="wm_mdicascade-message"></a>Mensagem do WM \_ MDICASCADE

Um aplicativo envia a mensagem do **WM \_ MDICASCADE** para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas em um formato em cascata.


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O comportamento em cascata. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                          | Significado                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_ SKIPDISABLED**</dt> <dt>0x0002</dt> </dl> | Impede que janelas filho MDI desabilitadas sejam colocadas em cascata. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_**</dt> <dt>0X0004</dt> de ZORDER </dl>                   | Organiza as janelas na ordem Z.<br/>                          |



 

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

[**MDIICONARRANGE do WM \_**](wm-mdiiconarrange.md)
</dt> <dt>

[**MDITILE do WM \_**](wm-mditile.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




