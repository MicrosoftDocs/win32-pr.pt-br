---
title: TVN_ASYNCDRAW código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore para seu pai quando o desenho de um ícone ou sobreposição falhou. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748249"
---
# <a name="tvn_asyncdraw-notification-code"></a>Código de notificação do TVN \_ ASYNCDRAW

Enviado por um controle de exibição de árvore para seu pai quando o desenho de um ícone ou sobreposição falhou. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . A estrutura **NMTVASYNCDRAW** contém o motivo pelo qual o empate falhou.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O controle de exibição de árvore deve ter o estilo estendido de [**TVs \_ ex \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) . Observe que isso é equivalente ao sinalizador LVN ASYNCDRAWN da exibição de lista \_ e seu estilo correspondente.

Esse controle não é desenhado de forma assíncrona. Assíncrona é usado no contexto que o controle de exibição de árvore não extrai de forma síncrona uma imagem se ela não estiver disponível. (Por exemplo, a imagem pode não estar disponível se o controle de exibição de árvore usar uma lista de imagens esparsas, uma vez que a imagem pode ser descarregada.) Em vez disso, quando uma imagem não está disponível, o controle, de forma síncrona, solicita ao pai qual ação tomar enviando o pai uma \_ notificação TVN ASYNCDRAW com uma estrutura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . O membro de **RH** desta estrutura descreve o motivo pelo qual o desenho do controle falhou. Um resultado de **RH** de E \_ pendente significa que a imagem não está presente (a imagem precisa ser extraída). Êxito indica que a imagem está presente, mas não na qualidade da imagem necessária.

O pai define o membro **dwRetFlags** da estrutura para informar ao controle como proceder. Por exemplo, o pai pode retornar outra imagem, no membro **iRetImageIndex** , para o controle desenhar. Nesse caso, o pai define o membro **dwRetFlags** como ADRF \_ DRAWIMAGE. Se o controle encontrar a imagem retornada não tiver sido extraído, ainda outra \_ notificação de ASYNCDRAW TVN poderá ser enviada pelo controle.

Se uma imagem não estiver disponível, a ideia por trás da assíncrona é permitir que o pai faça a extração em segundo plano para que a extração não bloqueie o thread da interface do usuário, ou seja, o thread no qual o controle está. O pai pode retornar ADRF \_ DRAWNOTHING ao controle e, em seguida, iniciar um thread em segundo plano para extrair o ícone. Depois de extraído, o pai pode definir o ícone no controle TreeView com macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem). Isso faz com que a exibição de árvore invalidasse o item e, eventualmente, repinte-o com a imagem extraída na lista de imagens.

O exemplo de código a seguir, a ser usado como parte de um programa maior, mostra como um pai pode processar dois códigos de retorno possíveis nessa notificação por um controle e decidir qual ação deve ser tomada pelo controle. A configuração de **dwRetFlags** não é mostrada.


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





