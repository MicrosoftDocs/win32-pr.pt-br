---
title: Páginas de propriedades para uso com especificadores de exibição
description: Active Directory Domain Services fornecer um mecanismo para adicionar páginas à folha de propriedades exibida para um objeto de diretório a partir dos snap-ins administrativos Active Directory ou do shell do Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- exibir o anúncio de especificadores, páginas de propriedades para uso com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823641"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Páginas de propriedades para uso com especificadores de exibição

Active Directory Domain Services fornecer um mecanismo para adicionar páginas à folha de propriedades exibida para um objeto de diretório a partir dos snap-ins administrativos Active Directory ou do shell do Windows. Para adicionar uma página à folha de propriedades, implemente uma extensão de folha de propriedades.

## <a name="developer-audience"></a>Público do desenvolvedor

Esta documentação pressupõe que o leitor esteja familiarizado com a operação COM e o desenvolvimento de componentes usando o C++. No momento, não é possível criar uma extensão de folha de propriedades Active Directory usando Visual Basic.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Criando uma extensão de folha de propriedades Active Directory

Uma *extensão de folha de propriedades* é um servidor em processamento com que implementa determinadas interfaces e é registrado com Active Directory Domain Services. Para criar uma extensão de folha de propriedades, execute as etapas a seguir.

**Para criar uma extensão de folha de propriedades Active Directory**

1.  Crie a DLL de extensão da folha de propriedades. Uma extensão de folha de propriedades é um servidor em processamento COM que, no mínimo, implementa as interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Para obter mais informações, consulte [implementando o objeto com da página de propriedades](implementing-the-property-page-com-object.md).
2.  Instale a extensão da folha de propriedades nos computadores em que a extensão da folha de propriedades deve ser usada. Para fazer isso, crie um pacote de Microsoft Windows Installer para a DLL de extensão da folha de propriedades e implante o pacote adequadamente usando a política de grupo. Para obter mais informações, consulte [distribuindo componentes da interface do usuário](distributing-user-interface-components.md).
3.  Registre a extensão da folha de propriedades no registro do Windows e com Active Directory Domain Services. Para obter mais informações, consulte [registrando o objeto com da página de propriedades em um especificador de exibição](registering-the-property-page-com-object-in-a-display-specifier.md).

 

 