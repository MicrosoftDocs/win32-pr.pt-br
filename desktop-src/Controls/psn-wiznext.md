---
title: PSN_WIZNEXT código de notificação (Prsht. h)
description: Notifica uma página que o usuário clicou no botão Avançar em um assistente. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT código de notificação Windows controles
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dead2de1e21631b2b8e13cb54e3ee45d5d3bc29f2234380c31ec134c3790eae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169626"
---
# <a name="psn_wiznext-notification-code"></a>Código de notificação do PSN \_ WIZNEXT

Notifica uma página que o usuário clicou no botão **Avançar** em um assistente. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades. O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne 0 para permitir que o assistente vá para a próxima página. Retorne-1 para impedir que o assistente altere as páginas. Para exibir uma página específica, retorne seu identificador de recurso de caixa de diálogo. Se a caixa de diálogo tiver sido especificada com o sinalizador [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , essa notificação retornará o ponteiro para o modelo da caixa de diálogo.

## <a name="remarks"></a>Comentários

Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o valor **\_ MSGRESULT DWL** e retornar **true**. Por exemplo:

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação PSN WIZNEXT é enviado. Você pode adicionar, inserir ou remover páginas em resposta a esses códigos de notificação, mas deve ser levado um cuidado especial se você inserir ou remover páginas antes da página atual.

 

Se você inserir ou remover páginas antes da página atual, deverá retornar (por meio de **DWL \_ MSGRESULT**) um valor diferente de zero para especificar a página nova desejada. No entanto, observe que se você inserir ou remover uma página que está localizada antes da página atual (que tem um índice menor do que a página atual), [PSN \_ KILLACTIVE](psn-killactive.md) poderá ser enviada para a página errada.

Por esse motivo, é recomendável que os assistentes que adicionam e removem páginas dinamicamente em resposta a PSN \_ WIZNEXT e [PSN \_ WIZBACK](psn-wizback.md) façam isso somente para páginas no final da lista. Se você quiser que o assistente remova as páginas com precisão, mantenha as páginas dinâmicas no final da lista e volte para páginas permanentes antes de excluí-las.

Por exemplo, suponha que um assistente consiste em uma página introdutória, uma série de páginas dinâmicas e uma página de conclusão, e você deseja excluir as páginas dinâmicas quando o usuário atingir a página de conclusão.

1.  O assistente começaria com duas páginas, "introdução" e "conclusão". O usuário começa na página "introdução".
    1.  Introdução (o usuário está aqui)
    2.  Completion
2.  Quando o usuário sai da "introdução", o assistente adiciona as páginas dinâmicas e coloca o usuário na primeira página dinâmica retornando (por meio de **DWL \_ MSGRESULT**) o identificador da caixa de diálogo da página "dinâmico 1". Neste exemplo, há três páginas dinâmicas.
    1.  Introdução
    2.  Completion
    3.  Dinâmico 1 (o usuário está aqui)
    4.  Dinâmico 2
    5.  Dinâmico 3
3.  Depois que o usuário navega pelas páginas dinâmicas para "Dynamic 3" e, em seguida, navega para a próxima página, o aplicativo deve posicionar o usuário na página "conclusão". Novamente, isso é feito retornando (por meio de **DWL \_ MSGRESULT**) o identificador da caixa de diálogo da página "conclusão".
    1.  Introdução
    2.  Conclusão (o usuário está aqui)
    3.  Dinâmico 1
    4.  Dinâmico 2
    5.  Dinâmico 3
4.  O aplicativo pode, então, remover as três páginas dinâmicas (numeradas de três a cinco) com segurança.
    1.  Introdução
    2.  Conclusão (o usuário está aqui)

Observe que essa técnica será necessária apenas se o assistente remover as páginas dinamicamente. Se o assistente Adicionar apenas páginas dinamicamente, esse processo não será necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

