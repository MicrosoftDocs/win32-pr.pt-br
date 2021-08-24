---
title: Mensagem de TTM_ADJUSTRECT (commctrl. h)
description: Calcula o retângulo de exibição de texto de um controle de dica de ferramenta de seu retângulo de janela ou o retângulo da janela de dica de ferramenta necessário para exibir um retângulo de exibição de texto especificado.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- controles de Windows de mensagem de TTM_ADJUSTRECT
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba5a6719bcbd820d94b6d736a12644f8b2539cc81064f942616c62bce55823f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769526"
---
# <a name="ttm_adjustrect-message"></a>\_Mensagem TTM ADJUSTRECT

Calcula o retângulo de exibição de texto de um controle de dica de ferramenta de seu retângulo de janela ou o retângulo da janela de dica de ferramenta necessário para exibir um retângulo de exibição de texto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica qual operação deve ser executada. Se for **true**, *lParam* será usado para especificar um retângulo de exibição de texto e receberá o retângulo de janela correspondente. Se for **false**, *lParam* será usado para especificar um retângulo de janela e receberá o retângulo de exibição de texto correspondente.

</dd> <dt>

*lParam* 
</dt> <dd>

Estrutura **Rect** para manter um retângulo de janela de dica de ferramenta ou um retângulo de exibição de texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará um valor diferente de zero se o retângulo for ajustado com êxito e retornará zero se ocorrer um erro.

## <a name="remarks"></a>Comentários

Essa mensagem é particularmente útil quando você deseja usar um controle ToolTip para exibir o texto completo de uma cadeia de caracteres que geralmente é truncada. Normalmente, ele é usado com controles ListView e TreeView. Normalmente, você envia essa mensagem em resposta a um código de notificação [TTN \_ show](ttn-show.md) para que você possa posicionar o controle ToolTip corretamente.

O retângulo da janela de dica de ferramenta é um pouco maior do que o retângulo de exibição de texto que limita a cadeia de dica de ferramenta. A origem da janela também é deslocada para cima e para a esquerda da origem do retângulo de exibição de texto. Para posicionar o retângulo de exibição de texto, você deve calcular o retângulo de janela correspondente e usar esse retângulo para posicionar a dica de ferramenta. **TTM \_ O ADJUSTRECT** lida com esse cálculo para você.

Se você definir *wParam* como **true**, **TTM \_ ADJUSTRECT** usará o tamanho e a posição do retângulo de exibição de texto de dica de ferramenta desejado e retornará o tamanho e a posição da janela de dica de ferramenta necessária para exibir o texto na posição especificada. Se você definir *wParam* como **false**, poderá especificar um retângulo de janela de dica de ferramenta e **TTM \_ ADJUSTRECT** retornará o tamanho e a posição de seu retângulo de texto.

O fragmento de código a seguir ilustra o uso da mensagem **TTM \_ ADJUSTRECT** para posicionar um controle ToolTip para exibir o texto completo da cadeia de caracteres de um controle no lugar de uma cadeia de caracteres truncada. A função **GetMyItemRect** definida pelo aplicativo retorna o retângulo de texto que será necessário para exibir o texto da dica de ferramenta diretamente sobre a cadeia de caracteres truncada. Os detalhes de como essa função é implementada dependerão do controle específico. **TTM \_ ADJUSTRECT** é usado para enviar este retângulo de texto para o controle ToolTip. Ele retorna um retângulo de janela dimensionado e posicionado adequadamente que é usado para posicionar a janela de dica de ferramenta.


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





