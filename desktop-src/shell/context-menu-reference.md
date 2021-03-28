---
description: Este tópico lista os principais elementos de programação usados com menus de atalho (contexto) e manipuladores de menu de atalho. Manipuladores de menu de atalho, que também são conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Referência do menu de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb1552c8f2f383b08984e9142e464b6831a3c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164315"
---
# <a name="shortcut-menu-reference"></a>Referência do menu de atalho

Este tópico lista os principais elementos de programação usados com menus de atalho (contexto) e manipuladores de menu de atalho. Manipuladores de menu de atalho, que também são conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo.

## <a name="about-shortcut-menu-implemetation"></a>Sobre o menu de atalho implemetation

É altamente recomendável que você implemente um menu de atalho usando um dos métodos de verbo estáticos. Examine as seguintes instruções:

-   Para usar um método verbo estático para implementar um menu de atalho, consulte a seção "Personalizando um menu de atalho usando verbos estáticos" de [criando manipuladores de menu de atalho](context-menu-handlers.md).
-   Para obter um comportamento dinâmico para verbos estáticos no Windows 7 e posterior, consulte "obtendo comportamento dinâmico para verbos estáticos" na [criação de manipuladores de menu de atalho](context-menu-handlers.md).
-   Para obter detalhes sobre a implementação de verbo estático e quais verbos dinâmicos evitar, consulte [escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md).
-   Se você precisar estender o menu de atalho para um tipo de arquivo registrando um verbo dinâmico para o tipo de arquivo, siga as instruções fornecidas em [Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md).

### <a name="interfaces"></a>Interfaces



| Tópico                                        | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Expõe métodos que criam ou mesclam um menu de atalho associado a um objeto Shell.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Expõe métodos que criam ou mesclam um menu de atalho (contexto) associado a um objeto Shell. Estende [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) adicionando um método que permite que os objetos de cliente manipulem mensagens associadas a itens de menu extraídos pelo proprietário.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Expõe métodos que criam ou mesclam um menu de atalho associado a um objeto Shell. Permite que os objetos de cliente manipulem mensagens associadas a itens de menu desenhados pelo proprietário e estende o [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) aceitando um valor de retorno dessa manipulação de mensagens.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Expõe um método que habilita o retorno de chamada de um menu de contexto. Por exemplo, para adicionar um ícone de escudo a um **MenuItem** que requer elevação.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Implementado pelo modo de exibição de pasta padrão criado usando [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Uma implementação de [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) dá suporte a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) e qualquer encaminhamento de mensagem necessário para essa função. O **IContextMenuSite** normalmente também atualiza a barra de status.<br/> |



 

### <a name="functions"></a>Funções



| Tópico                                                            | Sumário                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Cria um menu de contexto para um grupo selecionado de objetos de pasta de arquivos.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Define o protótipo para a função de retorno de chamada que recebe mensagens da implementação do menu de contexto padrão do Shell.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Cria um objeto que representa a implementação do menu de contexto padrão do Shell.<br/>                                           |



 

### <a name="structures"></a>Estruturas



| Tópico                                                  | Sumário                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Contém as informações necessárias para [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para invocar um comando de menu de atalho.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Contém informações estendidas sobre um comando de menu de atalho. Essa estrutura é uma versão estendida do [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) que permite o uso de valores Unicode.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Contém informações de menu de contexto usadas pelo [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).<br/>                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md)
</dt> <dt>

[Verbos e associações de arquivo](fa-verbs.md)
</dt> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla](verbs-best-practices.md)
</dt> <dt>

[Criando manipuladores de menu de atalho](context-menu-handlers.md)
</dt> <dt>

[Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
