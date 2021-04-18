---
description: Um conjunto de folhas de propriedades e páginas de propriedades que permitem ao usuário exibir e modificar os componentes de um descritor de segurança de objetos.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Editor de controle de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65117fe086b6a374dbd973f2cb657ec9c19cc3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751405"
---
# <a name="access-control-editor"></a>Editor de controle de acesso

O editor de controle de acesso é um conjunto de folhas de propriedades e páginas de propriedades que permitem ao usuário exibir e modificar os componentes do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto. O editor consiste em duas partes principais:

-   Uma [página de propriedades de segurança básica](basic-security-property-page.md) que fornece uma interface simples para editar as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na DACL (lista de controle de [*acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) de um objeto. Essa página pode incluir um botão **avançado** opcional que exibe a folha de propriedades segurança avançada.
-   Uma [folha de propriedades de segurança avançada](advanced-security-property-sheet.md) com páginas de propriedades que permitem ao usuário editar a SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema do objeto, alterar o proprietário do objeto ou executar a edição avançada da DACL do objeto.

A função [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) cria a página de propriedades de segurança básica. Você pode usar a função [**folha**](/windows/win32/api/prsht/nf-prsht-propertysheeta) ou a mensagem de [**PSM \_ ADDPAGE**](../controls/psm-addpage.md) para adicionar essa página a uma folha de propriedades.

Como alternativa, você pode usar a função [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) para exibir uma folha de propriedades que contém a página de propriedades de segurança básica.

Para [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) e [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity), o chamador deve passar um ponteiro para uma implementação da interface [**ISecurityInformation**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) . O editor de controle de acesso chama os métodos dessa interface para recuperar informações de controle de acesso sobre o objeto que está sendo editado e para passar a entrada do usuário de volta para seu aplicativo. Os métodos **ISecurityInformation** têm as seguintes finalidades:

-   Para inicializar as páginas de propriedades.

    Sua implementação do método [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) passa uma estrutura [**de \_ \_ informações de objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) para o editor. Essa estrutura especifica as páginas de propriedades que você deseja que o editor exiba e outras informações que determinam as opções de edição disponíveis para o usuário.

-   Para fornecer informações de segurança sobre o objeto que está sendo editado.

    A implementação de [**getSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) passa o [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) inicial do objeto para o editor. Os métodos [**GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) e [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) fornecem informações sobre os direitos de acesso do objeto. O método [**GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) fornece informações sobre como as ACEs do objeto podem ser herdadas por objetos filho.

-   Para passar a entrada do usuário de volta para seu aplicativo.

    Quando o usuário clica em **OK** ou em **aplicar**, o editor chama o método [**setsecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) para retornar um descritor de segurança que contém as alterações do usuário.

 

 
