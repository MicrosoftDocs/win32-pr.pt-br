---
description: Este tópico lista os principais elementos de programação usados com menus de atalho (contexto) e manipuladores de menu de atalho. Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Referência de menu de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f80b62b88750200456da76c22017b3f18fbba584272dc028809771c807ad85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090766"
---
# <a name="shortcut-menu-reference"></a>Referência de menu de atalho

Este tópico lista os principais elementos de programação usados com menus de atalho (contexto) e manipuladores de menu de atalho. Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo.

## <a name="about-shortcut-menu-implemetation"></a>Sobre a implemetação de menu de atalho

É fortemente incentivado que você implemente um menu de atalho usando um dos métodos verbais estáticos. Leia as seguintes instruções:

-   Para usar um método de verbo estático para implementar um menu de atalho, consulte a seção "Personalização de um menu de atalho usando verbos estáticos" de Criando manipuladores de [menu de atalho.](context-menu-handlers.md)
-   Para obter o comportamento dinâmico para verbos estáticos no Windows 7 e posterior, consulte "Obter comportamento dinâmico para verbos estáticos" em Criando manipuladores de [menu de atalho](context-menu-handlers.md).
-   Para obter detalhes sobre a implementação de verbo estático e quais verbos dinâmicos devem ser evitados, consulte Escolhendo um verbo estático ou [dinâmico para o menu de atalho.](shortcut-choose-method.md)
-   Se você tiver que estender o menu de atalho para um tipo de arquivo registrando um verbo dinâmico para o tipo de arquivo, siga as instruções fornecidas em Personalização de um menu de atalho usando [verbos dinâmicos.](shortcut-menu-using-dynamic-verbs.md)

### <a name="interfaces"></a>Interfaces



| Tópico                                        | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icontextmenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Expõe métodos que criam ou mesclam um menu de atalho associado a um objeto Shell.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Expõe métodos que criam ou mesclam um menu de atalho (contexto) associado a um objeto Shell. Estende [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) adicionando um método que permite que objetos cliente manipularem mensagens associadas a itens de menu desenhados pelo proprietário.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Expõe métodos que criam ou mesclam um menu de atalho associado a um objeto Shell. Permite que os objetos cliente manipulam mensagens associadas a itens de menu desenhados pelo proprietário e estende [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) aceitando um valor de retorno dessa manipulação de mensagens.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Expõe um método que habilita o retorno de chamada de um menu de contexto. Por exemplo, para adicionar um ícone de blindagem a **um menuItem que requer** elevação.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Implementado pela exibição de pasta padrão criada usando [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Uma implementação de [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) dá suporte a [**IContextMenu::QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) e a qualquer encaminhamento de mensagem necessário para essa função. **IContextMenuSite** normalmente atualiza a barra de status também.<br/> |



 

### <a name="functions"></a>Funções



| Tópico                                                            | Sumário                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Cria um menu de contexto para um grupo selecionado de objetos de pasta de arquivos.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Define o protótipo da função de retorno de chamada que recebe mensagens da implementação de menu de contexto padrão do Shell.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Cria um objeto que representa a implementação de menu de contexto padrão do Shell.<br/>                                           |



 

### <a name="structures"></a>Estruturas



| Tópico                                                  | Sumário                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Contém informações necessárias para [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para invocar um comando de menu de atalho.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Contém informações estendidas sobre um comando de menu de atalho. Essa estrutura é uma versão estendida [**de CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) que permite o uso de valores Unicode.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Contém informações de menu de contexto usadas [**por SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).<br/>                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md)
</dt> <dt>

[Verbos e associações de arquivo](fa-verbs.md)
</dt> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e vários verbos de seleção](verbs-best-practices.md)
</dt> <dt>

[Como Criar Manipuladores do Menu de Atalho](context-menu-handlers.md)
</dt> <dt>

[Personalização de um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
