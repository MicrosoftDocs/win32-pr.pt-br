---
description: Cada usuário e SID (identificador de segurança de grupo) em um token de acesso tem um conjunto de atributos que controlam como o sistema usa o SID em uma verificação de acesso. A tabela a seguir lista os atributos que controlam a verificação de acesso.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Atributos de SID em um token de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a93e180c8c6ffe03a26591d5b9f722c2266356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647460"
---
# <a name="sid-attributes-in-an-access-token"></a>Atributos de SID em um token de acesso

Cada usuário e Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) de grupo) em um token de [*acesso*](/windows/desktop/SecGloss/a-gly) tem um conjunto de atributos que controlam como o sistema usa o Sid em uma verificação de acesso. A tabela a seguir lista os atributos que controlam a verificação de acesso.



| Atributo                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_grupo se \_ habilitado              | Um SID com esse atributo está habilitado para verificações de acesso. Quando o sistema executa uma verificação de acesso, ele verifica as ACEs (entradas de controle de [*acesso*](/windows/desktop/SecGloss/a-gly) ) permitidas e com acesso negado que se aplicam a um dos SIDs habilitados no token de acesso. Um SID sem esse atributo é ignorado durante uma verificação de acesso, a menos que o \_ grupo se \_ use \_ para \_ negar \_ somente atributo esteja definido.<br/> |
| \_ \_ uso de grupo \_ se \_ somente para negação \_ | Um SID com esse atributo é um SID somente de negação. Quando o sistema executa uma verificação de acesso, ele verifica as ACEs com acesso negado que se aplicam ao SID, mas ignora as ACEs de acesso permitido para o SID. Se esse atributo for definido, o \_ atributo habilitado para grupo se \_ não será definido e o Sid não poderá ser reabilitado.<br/>                                                                                                                                                          |



 

Para definir ou limpar o \_ atributo habilitado para grupo se \_ de um SID de grupo, use a função [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) . Não é possível desabilitar um SID de grupo que tenha o \_ atributo do grupo se \_ obrigatório. Você não pode usar **AdjustTokenGroups** para desabilitar o Sid de usuário de um token de acesso.

Para determinar se um SID está habilitado em um token, ou seja, se ele tem o \_ atributo do grupo se \_ habilitado, chame a função [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) .

Para definir o \_ uso do grupo se \_ \_ para \_ negação \_ somente de um Sid, inclua o Sid na lista de SIDs somente de negação que você especificar ao chamar a função [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . **CreateRestrictedToken** pode aplicar o \_ grupo se \_ use \_ somente para o \_ \_ atributo Deny para qualquer Sid, incluindo o Sid de usuário e os SIDs de grupo que têm o \_ atributo do grupo se \_ obrigatório. No entanto, você não pode remover o atributo somente negação de um SID, nem pode usar [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) para definir o \_ atributo habilitado para grupo se \_ em um SID somente de negação.

Para obter os atributos de um SID, chame a função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) com o valor tokenGroups. A função retorna uma matriz de estruturas de [**\_ \_ atributos e Sid**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) que identificam os SIDs de grupo e seus atributos.

 

