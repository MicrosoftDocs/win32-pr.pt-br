---
description: A página inicial da folha de propriedades exibida pela função EditSecurity. Você também pode usar a função CreateSecurityPage para criar uma página de propriedades de segurança básica para inserir em sua própria folha de propriedades.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Página de propriedades de segurança básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8628b0b096e24a3a7baef94f5ab9913c2cd89825bb15bf6b19d18cd81d1033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783703"
---
# <a name="basic-security-property-page"></a>Página de propriedades de segurança básica

A página de propriedades de segurança básica é a página inicial da folha de propriedades exibida pela [**função EditSecurity.**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) Você também pode usar a [**função CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) para criar uma página de propriedades de segurança básica para inserir em sua própria folha de propriedades.

A página de propriedades exibe uma lista dos [administradores](trustees.md) nomeados nas ACEs [*(entradas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) da DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) do objeto. A página também contém uma lista dos direitos de acesso com suporte pelo objeto . Quando o usuário seleciona um nome na lista de administradores, as caixas de seleção ao lado de cada direito de acesso indicam os direitos permitidos ou negados para esse usuário confiável. Em seguida, o usuário pode selecionar ou des marcar as caixas de seleção para modificar os direitos de acesso do usuário confiável. O usuário também pode adicionar ou remover os usuários de confiança da lista.

A página de propriedades de segurança básica não pode exibir ACEs complexas, como [ACEs específicas do](object-specific-aces.md)objeto ou informações de herança ACE. Para permitir que o usuário veja ou edite essas informações, você pode incluir um **botão** Avançado na página de segurança básica. O usuário pode clicar no **botão Avançado** para exibir uma folha de propriedades de [segurança avançada](advanced-security-property-sheet.md). Essa folha de propriedades tem páginas de propriedades que permitem que o usuário edite a SACL [*(lista*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema) do objeto, altere o proprietário do objeto ou execute a edição avançada da DACL do objeto. Para exibir o **botão** Avançado, de definir o sinalizador SI ADVANCED na estrutura SI OBJECT INFO retornada pela implementação \_ [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

Você pode usar o **membro pszPageTitle** da estrutura [**SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) para especificar o título da página de propriedades de segurança básica. O título padrão é **Segurança**.

 

 
