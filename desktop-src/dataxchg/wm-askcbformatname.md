---
title: Mensagem de WM_ASKCBFORMATNAME (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência para solicitar o nome de um formato de área de transferência do CF \_ OWNERDISPLAY.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- Troca de dados de mensagem WM_ASKCBFORMATNAME
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085349"
---
# <a name="wm_askcbformatname-message"></a>Mensagem do WM \_ ASKCBFORMATNAME

Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência para solicitar o nome de um formato de área de transferência do [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) .

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tamanho, em caracteres, do buffer apontado pelo parâmetro *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que deve receber o nome do formato da área de transferência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Em resposta a essa mensagem, o proprietário da área de transferência deve copiar o nome do formato de exibição de proprietário para o buffer especificado, não excedendo o tamanho do buffer especificado pelo parâmetro *wParam* .

Uma janela do Visualizador da área de transferência envia essa mensagem para o proprietário da área de transferência para determinar o nome do formato de [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) , por exemplo, para inicializar um menu que lista os formatos disponíveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral da área de transferência](clipboard.md)
</dt> </dl>

 

