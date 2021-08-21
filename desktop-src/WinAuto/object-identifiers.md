---
title: Identificadores de objeto (WinUser. h)
description: Este tópico descreve os identificadores de objeto do Microsoft Acessibilidade Ativa, os valores de 32 bits que identificam categorias de objetos acessíveis em uma janela.
ms.assetid: dc1603f8-29e5-4acd-817a-c6957feaff6c
topic_type:
- apiref
api_name:
- OBJID_ALERT
- OBJID_CARET
- OBJID_CLIENT
- OBJID_CURSOR
- OBJID_HSCROLL
- OBJID_NATIVEOM
- OBJID_MENU
- OBJID_QUERYCLASSNAMEIDX
- OBJID_SIZEGRIP
- OBJID_SOUND
- OBJID_SYSMENU
- OBJID_TITLEBAR
- OBJID_VSCROLL
- OBJID_WINDOW
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b91bf70333d4ba7d607e465851f7f217aec43b0a081ec020017321fe30a7ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565061"
---
# <a name="object-identifiers-winuserh"></a>Identificadores de objeto (WinUser. h)

Este tópico descreve os identificadores de objeto do Microsoft Acessibilidade Ativa, os valores de 32 bits que identificam *categorias* de objetos acessíveis em uma janela. Os Microsoft Acessibilidade Ativa Servers e os provedores de automação da interface do usuário da Microsoft usam os identificadores de objeto para determinar o objeto ao qual uma solicitação de mensagem do [**WM \_ GetObject**](wm-getobject.md) se refere.

Os clientes recebem esses valores em sua função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e os usam para identificar partes de uma janela. Os servidores usam esses valores para identificar as partes correspondentes de uma janela ao chamar [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ou ao responder à mensagem do [**WM \_ GetObject**](wm-getobject.md) .

Os servidores podem definir IDs de objeto personalizados para identificar outras categorias de objetos em seus aplicativos. IDs de objeto personalizado devem receber valores positivos porque o Microsoft Acessibilidade Ativa reserva zero e todos os valores negativos para os identificadores de objeto padrão a seguir.

As constantes a seguir são definidas em winuser. h:



| Constante                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**alerta de OBJID \_**</dt> </dl>                                     | Um alerta associado a uma janela ou a um aplicativo. As caixas de mensagens fornecidas pelo sistema são os únicos elementos da interface do usuário que enviam eventos com esse identificador de objeto. Os aplicativos de servidor não podem usar as funções **AccessibleObjectFrom**_X_ com esse identificador de objeto. Esse é um problema conhecido com o Microsoft Acessibilidade Ativa.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**OBJID \_ circunflexo**</dt> </dl>                                     | A barra de inserção de texto (circunflexo) na janela.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**\_cliente OBJID**</dt> </dl>                                  | A área do cliente da janela. Na maioria dos casos, o sistema operacional controla os elementos de quadro e o objeto de cliente contém todos os elementos que são controlados pelo aplicativo. Os servidores processam apenas as mensagens do [**WM \_ GetObject**](wm-getobject.md) nas quais o *lParam* é OBJID \_ Client, OBJID \_ Window ou um identificador de objeto personalizado.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**\_cursor OBJID**</dt> </dl>                                  | O ponteiro do mouse. Há apenas um ponteiro do mouse no sistema e não é um filho de nenhuma janela.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | A barra de rolagem horizontal da janela.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ NATIVEOM**</dt> </dl>                            | Em resposta a esse identificador de objeto, aplicativos de terceiros podem expor seu próprio modelo de objeto. Aplicativos de terceiros podem retornar qualquer interface COM em resposta a esse identificador de objeto.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**\_menu OBJID**</dt> </dl>                                        | A barra de menus da janela.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ QUERYCLASSNAMEIDX**</dt> </dl> | Um identificador de objeto que Oleacc.dll usa internamente. Para obter mais informações, consulte o [Apêndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**OBJID \_ SIZEGRIP**</dt> </dl>                            | A alça de tamanho da janela: um componente de quadro opcional localizado no canto inferior direito do quadro da janela.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**\_som OBJID**</dt> </dl>                                     | Um objeto de som. Os objetos de som não têm locais de tela ou filhos, mas têm atributos de nome e estado. Eles são filhos do aplicativo que está reproduzindo o som.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ SYSMENU**</dt> </dl>                               | Menu do sistema da janela.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**OBJID \_ TITLEBAR**</dt> </dl>                            | A barra de título da janela.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**OBJID \_ VSCROLL**</dt> </dl>                               | A barra de rolagem vertical da janela.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**\_janela OBJID**</dt> </dl>                                  | A própria janela, em vez de um objeto filho.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





