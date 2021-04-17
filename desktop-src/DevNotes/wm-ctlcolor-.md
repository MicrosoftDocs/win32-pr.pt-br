---
description: A mensagem do WM \_ CTLCOLOR é usada em versões de 16 bits do Windows para alterar o esquema de cores das caixas de listagem, as caixas de listagem de caixas de combinação, caixas de mensagens, controles de botão, controles de edição, controles estáticos e caixas de diálogo. Observação para obter informações relacionadas a essa mensagem e as versões de 32 bits do Windows, consulte comentários.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Mensagem de WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769132"
---
# <a name="wm_ctlcolor-message"></a>Mensagem do WM \_ CTLCOLOR

A mensagem do **WM \_ CTLCOLOR** é usada em versões de 16 bits do Windows para alterar o esquema de cores das caixas de listagem, as caixas de listagem de caixas de combinação, caixas de mensagens, controles de botão, controles de edição, controles estáticos e caixas de diálogo.

> [!Note]  
> Para obter informações relacionadas a essa mensagem e as versões de 32 bits do Windows, consulte comentários.

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela de destino.

</dd> <dt>

*wParam* 
</dt> <dd>

Um identificador para um contexto de exibição (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para uma janela filho (controle).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele retornará um identificador para um pincel. O sistema usa o pincel para pintar o plano de fundo do controle.

## <a name="remarks"></a>Comentários

A mensagem do **WM \_ CTLCOLOR** do Windows de 16 bits foi substituída por notificações mais específicas. Essas substituições incluem o seguinte:

-   [**CTLCOLORBTN do WM \_**](../controls/wm-ctlcolorbtn.md)
-   [**CTLCOLOREDIT do WM \_**](../controls/wm-ctlcoloredit.md)
-   [**CTLCOLORDLG do WM \_**](../dlgbox/wm-ctlcolordlg.md)
-   [**CTLCOLORLISTBOX do WM \_**](../controls/wm-ctlcolorlistbox.md)
-   [**CTLCOLORSCROLLBAR do WM \_**](../controls/wm-ctlcolorscrollbar.md)
-   [**CTLCOLORSTATIC do WM \_**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WindowsX. h</dt> </dl> |



 

 
