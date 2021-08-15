---
description: Um conjunto de folhas de propriedades e páginas de propriedades que permitem que o usuário veja e modifique os componentes de um descritor de segurança de objetos.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Editor de Controle de Acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ed7c210c747278d35537fc010c66b60f0057d9a61b407eb04e993f8928f2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914674"
---
# <a name="access-control-editor"></a>Editor de Controle de Acesso

O editor de controle de acesso é um conjunto de folhas de propriedades e páginas de propriedades que permitem que o usuário veja e modifique os componentes do [*descritor de segurança de um objeto*](/windows/desktop/SecGloss/s-gly). O editor consiste em duas partes principais:

-   Uma [página de](basic-security-property-page.md) propriedade de segurança básica que fornece uma interface simples para editar as ACEs (entradas de controle de acesso) na DACL (lista de controle de acesso discricionário) de um objeto. [](/windows/desktop/SecGloss/a-gly) [](/windows/desktop/SecGloss/d-gly) Esta página pode incluir um botão **Avançado** opcional que exibe a folha de propriedades de segurança avançada.
-   Uma folha de propriedades de segurança avançada com páginas de propriedades que permitem que o usuário edite [a](advanced-security-property-sheet.md) SACL [*(lista*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema) do objeto, altere o proprietário do objeto ou execute a edição avançada da DACL do objeto.

A [**função CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) cria a página de propriedades de segurança básica. Em seguida, você pode usar a [**função PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) ou a mensagem [**\_ ADDPAGE do PSM**](../controls/psm-addpage.md) para adicionar essa página a uma folha de propriedades.

Como alternativa, você pode usar a [**função EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) para exibir uma folha de propriedades que contém a página de propriedades de segurança básica.

Para [**CreateSecurityPage e**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity), o chamador deve passar um ponteiro para uma implementação da interface [**ISecurityInformation.**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) O editor de controle de acesso chama os métodos dessa interface para recuperar informações de controle de acesso sobre o objeto que está sendo editado e passar a entrada do usuário de volta para seu aplicativo. Os **métodos ISecurityInformation** têm as seguintes finalidades:

-   Para inicializar as páginas de propriedades.

    Sua implementação do método [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) passa uma estrutura [**SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) para o editor. Essa estrutura especifica as páginas de propriedades que você deseja que o editor exibir e outras informações que determinam as opções de edição disponíveis para o usuário.

-   Para fornecer informações de segurança sobre o objeto que está sendo editado.

    Sua [**implementação getSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) passa o descritor de segurança inicial [*do objeto*](/windows/desktop/SecGloss/s-gly) para o editor. Os [**métodos GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) e [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) fornecem informações sobre os direitos de acesso do objeto. O [**método GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) fornece informações sobre como as ACEs do objeto podem ser herdadas por objetos filho.

-   Para passar a entrada do usuário de volta para seu aplicativo.

    Quando o usuário clica em **Ok** ou **Aplicar**, o editor chama o método [**SetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) para passar de volta um descritor de segurança que contém as alterações do usuário.

 

 
