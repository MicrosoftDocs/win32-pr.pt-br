---
title: WM_ASKCBFORMATNAME mensagem (Winuser.h)
description: Enviado ao proprietário da área de transferência por uma janela do visualizador de área de transferência para solicitar o nome de um formato de área de \_ transferência OWNERDISPLAY do CF.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME de dados de Exchange
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
ms.openlocfilehash: bfe96a2ddf4e6767c083ec2e3f4e3fc61bdde902ff93ce9a162ec7e93eb5bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991236"
---
# <a name="wm_askcbformatname-message"></a>Mensagem \_ WM ASKCBFORMATNAME

Enviado ao proprietário da área de transferência por uma janela do visualizador de área de transferência para solicitar o nome de um formato de área de transferência [**\_ OWNERDISPLAY**](standard-clipboard-formats.md) do CF.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tamanho, em caracteres, do buffer apontado pelo *parâmetro lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que deve receber o nome do formato da área de transferência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Em resposta a essa mensagem, o proprietário da área de transferência deve copiar o nome do formato de exibição do proprietário para o buffer especificado, não excedendo o tamanho do buffer especificado pelo *parâmetro wParam.*

Uma janela do visualizador da área de transferência envia essa mensagem para o proprietário da área de transferência para determinar o nome do formato [**\_ OWNERDISPLAY do CF,**](standard-clipboard-formats.md) por exemplo, para inicializar um menu listando os formatos disponíveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral da área de transferência](clipboard.md)
</dt> </dl>

 

