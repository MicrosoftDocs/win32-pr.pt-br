---
title: Sobre as interfaces de usuário do Active Directory Domain Services
description: Os administradores e usuários devem ser capazes de exibir e modificar objetos de serviço de diretório no Microsoft Active Directory Domain Services de uma interface do usuário.
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c451a44660aaadbf0021ff57e675736b797d8f3e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007279"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a>Sobre as interfaces de usuário do Active Directory Domain Services

Os administradores e usuários devem ser capazes de exibir e modificar objetos de serviço de diretório no Microsoft Active Directory Domain Services de uma interface do usuário. Os administradores gerenciam o servidor de Active Directory usando snap-ins diferentes do MMC (console de gerenciamento Microsoft), especificamente, os Active Directory Domain Services usuários e computadores, Active Directory Domain Services sites e serviços, Active Directory Domain Services domínios e relações de confiança e Active Directory Domain Services snap-ins do Gerenciador de esquema. O usuário final, se tiver concedido as permissões apropriadas, também poderá usar o Active Directory snap-ins do MMC para exibir objetos de diretório. O Shell do Windows também pode ser usado para exibir objetos de diretório. O Shell do Windows permite que os usuários procurem objetos armazenados no diretório do item de diretório em meus locais de rede na área de trabalho ou por meio de caixas de diálogo de pesquisa disponíveis no menu iniciar.

Active Directory Domain Services dá suporte a uma interface do usuário que se adapta para atender às necessidades de administradores e usuários finais. Active Directory Domain Services permite que você estenda a interface do usuário que representa as classes de objeto existentes, bem como as novas classes adicionadas ao esquema. Os elementos a seguir podem ser usados para controlar ou estender a interface do usuário para cada classe definida no esquema:

-   [Páginas de propriedades para uso com especificadores de exibição](property-pages-for-use-with-display-specifiers.md)
-   [Menus de contexto para uso com especificadores de exibição](context-menus-for-use-with-display-specifiers.md)
-   [Nomes de exibição de classe e atributo](class-and-attribute-display-names.md)
-   [Assistentes de criação de objeto](object-creation-wizards.md)
-   [Ícones de classe](class-icons.md)
-   [Exibindo contêineres como nós folha](viewing-containers-as-leaf-nodes.md)

A partir do Windows 2000, o sistema fornece objetos COM que implementam caixas de diálogo comuns para trabalhar com objetos de diretório. Essas caixas de diálogo fornecem uma interface do usuário comum sem a necessidade de reimplementar essas caixas de diálogo.

-   [Seletor de objetos de diretório](directory-object-picker.md)
-   [Navegador de domínio](domain-browser.md)
-   [Navegador de contêineres](container-browser.md)

Active Directory snap-ins administrativos, menus de contexto e páginas de propriedades podem ser estendidos usando snap-ins de extensão do MMC. Outras extensões do MMC, como painéis de controle, itens de namespace, barras de controles e barras de ferramentas também podem ser implementadas. Para obter mais informações, consulte [estendendo os snap-ins administrativos do Active Directory](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins).

 

 