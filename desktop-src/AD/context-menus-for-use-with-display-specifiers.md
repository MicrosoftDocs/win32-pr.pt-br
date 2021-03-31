---
title: Menus de contexto para uso com especificadores de exibição
description: Os snap-ins administrativos do MMC Active Directory e o Shell do Windows 2000 fornecem um mecanismo para adicionar um item ao menu de contexto exibido para objetos no Active Directory Domain Services.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- exibir o anúncio de especificadores, menus de contexto para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fbf703f17ea5c0fa7938365d485998be77e8d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917143"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Menus de contexto para uso com especificadores de exibição

Os snap-ins administrativos do MMC Active Directory e o Shell do Windows 2000 fornecem um mecanismo para adicionar um item ao menu de contexto exibido para objetos no Active Directory Domain Services. Um item de menu de contexto pode ser adicionado com a implementação de um servidor no proc conhecido como uma *extensão de menu de contexto*. Um item de menu de contexto também pode ser adicionado que invoca qualquer arquivo iniciado com a API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , como uma URL de aplicativo ou página da Web. Isso é conhecido como um *item de menu de contexto estático*.

## <a name="developer-audience"></a>Público do desenvolvedor

Esta documentação pressupõe que o leitor esteja familiarizado com a operação COM e o desenvolvimento de componentes usando o C++. No momento, não é possível criar uma extensão de menu de contexto Active Directory Domain Services usando o Microsoft Visual Basic.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Estendendo o menu de contexto com uma extensão de menu de contexto

Uma extensão de menu de contexto é um servidor em processamento COM que implementa determinadas interfaces e é registrado com Active Directory Domain Services.

**Para criar e instalar uma extensão de menu de contexto**

1.  Crie a DLL de extensão do menu de contexto. Uma extensão de menu de contexto é um servidor em processamento COM que, no mínimo, implementa as interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Para obter mais informações, consulte [Implementing the context menu com Object](implementing-the-context-menu-com-object.md).
2.  Instale a extensão de planilha de menu de contexto nos computadores em que a extensão do menu de contexto é usada. Isso é feito criando um pacote de Microsoft Windows Installer para a DLL de extensão do menu de contexto e implantando o pacote adequadamente usando a política de grupo. Para obter mais informações, consulte [distribuindo componentes da interface do usuário](distributing-user-interface-components.md).
3.  Registre a extensão do menu de contexto no registro do Windows e com Active Directory Domain Services. Para obter mais informações, consulte [registrando o objeto com do menu de contexto em um especificador de exibição](registering-the-context-menu-com-object-in-a-display-specifier.md).

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Estendendo o menu de contexto com um item de menu de contexto estático

Um item de menu de contexto estático pode ser usado para invocar qualquer arquivo iniciado com a API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , como uma URL de aplicativo ou página da Web. Para fazer isso, o item de menu de contexto estático para uma determinada classe de objeto deve ser registrado para que o item de menu de contexto estático seja adicionado ao menu de contexto de objetos dessa classe. Para obter mais informações, consulte [registrando um item de menu de contexto estático](registering-a-static-context-menu-item.md).

 

 