---
title: Páginas de propriedades para uso com especificadores de exibição
description: Active Directory Domain Services fornecer um mecanismo para adicionar páginas à folha de propriedades exibida para um objeto de diretório a partir dos snap-ins administrativos Active Directory ou Windows shell.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- exibir o anúncio de especificadores, páginas de propriedades para uso com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f813223aa88dce3b8bba867139bab476416cba1932c583e2e9be591de03fc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185180"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Páginas de propriedades para uso com especificadores de exibição

Active Directory Domain Services fornecer um mecanismo para adicionar páginas à folha de propriedades exibida para um objeto de diretório a partir dos snap-ins administrativos Active Directory ou Windows shell. Para adicionar uma página à folha de propriedades, implemente uma extensão de folha de propriedades.

## <a name="developer-audience"></a>Público do desenvolvedor

Esta documentação pressupõe que o leitor esteja familiarizado com a operação COM e o desenvolvimento de componentes usando o C++. No momento, não é possível criar uma extensão de folha de propriedades Active Directory usando Visual Basic.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Criando uma extensão de folha de propriedades Active Directory

Uma *extensão de folha de propriedades* é um servidor em processamento com que implementa determinadas interfaces e é registrado com Active Directory Domain Services. Para criar uma extensão de folha de propriedades, execute as etapas a seguir.

**Para criar uma extensão de folha de propriedades Active Directory**

1.  Crie a DLL de extensão da folha de propriedades. Uma extensão de folha de propriedades é um servidor em processamento COM que, no mínimo, implementa as interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Para obter mais informações, consulte [implementando o objeto com da página de propriedades](implementing-the-property-page-com-object.md).
2.  Instale a extensão da folha de propriedades nos computadores em que a extensão da folha de propriedades deve ser usada. para fazer isso, crie um pacote de Microsoft Windows Installer para a DLL de extensão da folha de propriedades e implante o pacote adequadamente usando a política de grupo. Para obter mais informações, consulte [distribuindo componentes da interface do usuário](distributing-user-interface-components.md).
3.  registre a extensão da folha de propriedades no registro de Windows e com Active Directory Domain Services. Para obter mais informações, consulte [registrando o objeto com da página de propriedades em um especificador de exibição](registering-the-property-page-com-object-in-a-display-specifier.md).

 

 