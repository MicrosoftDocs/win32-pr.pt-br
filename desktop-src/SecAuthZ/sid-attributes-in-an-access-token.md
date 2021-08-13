---
description: Cada SID (identificador de segurança) de usuário e grupo em um token de acesso tem um conjunto de atributos que controlam como o sistema usa o SID em uma verificação de acesso. A tabela a seguir lista os atributos que controlam a verificação de acesso.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Atributos SID em um token de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe504e190e6d6e884b8068eb23983b2bc506c7c8447a8db77fd3ddb9cdfb917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413416"
---
# <a name="sid-attributes-in-an-access-token"></a>Atributos SID em um token de acesso

Cada SID [*(identificador*](/windows/desktop/SecGloss/s-gly) de segurança) de usuário e grupo em um [*token*](/windows/desktop/SecGloss/a-gly) de acesso tem um conjunto de atributos que controlam como o sistema usa o SID em uma verificação de acesso. A tabela a seguir lista os atributos que controlam a verificação de acesso.



| Atributo                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ES GROUP \_ ENABLED              | Um SID com esse atributo está habilitado para verificações de acesso. Quando o sistema executa uma verificação de acesso, ele verifica se há ACEs [*(entradas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) permitidas e negadas ao acesso que se aplicam a um dos SIDs habilitados no token de acesso. Um SID sem esse atributo é ignorado durante uma verificação de acesso, a menos que o ES \_ GROUP USE FOR DENY ONLY seja \_ \_ \_ \_ definido.<br/> |
| \_ES USO \_ DE GRUPO SOMENTE PARA \_ \_ \_ NEGAR | Um SID com esse atributo é um SID somente negação. Quando o sistema executa uma verificação de acesso, ele verifica se há ACEs de acesso negado que se aplicam ao SID, mas ignora ACEs permitidas para o SID. Se esse atributo for definido, o atributo ES GROUP ENABLED não será definido e o \_ SID não poderá ser \_ reabilitar.<br/>                                                                                                                                                          |



 

Para definir ou limpar o ES GROUP ENABLED de um SID de \_ \_ grupo, use a [**função AdjustTokenGroups.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) Você não pode desabilitar um SID de grupo que tenha o ES \_ GROUP \_ MANDATORY. Você não pode usar **AdjustTokenGroups** para desabilitar o SID do usuário de um token de acesso.

Para determinar se um SID está habilitado em um token, ou seja, se ele tem o atributo ES GROUP ENABLED, chame a \_ \_ função [**CheckTokenMembership.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)

Para definir o atributo ES GROUP USE FOR DENY ONLY de um SID, inclua o SID na lista de SIDs somente negação que você especificar ao chamar \_ \_ a função \_ \_ \_ [**CreateRestrictedToken.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) **CreateRestrictedToken** pode aplicar o atributo ES GROUP USE FOR DENY ONLY a qualquer SID, incluindo o SID do usuário e os \_ \_ \_ \_ \_ SIDs de \_ grupo que têm o atributo ES GROUP \_ MANDATORY. No entanto, você não pode remover o atributo somente negação de um SID, nem pode usar [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) para definir o atributo ES GROUP ENABLED em um SID somente \_ \_ negação.

Para obter os atributos de um SID, chame a [**função GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) com o valor TokenGroups. A função retorna uma matriz de [**estruturas SID \_ AND \_ ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) que identificam os SIDs de grupo e seus atributos.

 

