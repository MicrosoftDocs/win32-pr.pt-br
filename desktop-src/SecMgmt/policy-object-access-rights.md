---
description: Lista e descreve os tipos de acesso do objeto de política.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Direitos de acesso ao objeto de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae22db51c28e76e7122a1f7baf781671d9cc445e253fb6df7d63f87e3f7e921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005094"
---
# <a name="policy-object-access-rights"></a>Direitos de acesso ao objeto de política

O objeto de [**política**](policy-object.md) tem os seguintes tipos de acesso específicos de objeto:



| Tipo de acesso                         | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ informações locais da exibição de política \_    | Esse tipo de acesso é necessário para ler as informações de política de segurança diversas do sistema de destino. Isso inclui a cota padrão, a auditoria, o estado do servidor e as informações de função e as informações de confiança. Esse tipo de acesso também é necessário para enumerar domínios, contas e [*privilégios*](/windows/desktop/SecGloss/p-gly)confiáveis. |
| \_obter \_ informações particulares \_ de política   | Esse tipo de acesso é necessário para exibir informações confidenciais, como os nomes das contas estabelecidas para relações de domínio confiáveis.                                                                                                                                                                                                                              |
| \_administrador de confiança de política \_                | Esse tipo de acesso é necessário para alterar as informações de domínio de conta ou domínio primário.                                                                                                                                                                                                                                                                             |
| \_limites de \_ \_ cota padrão do conjunto \_ de políticas | Defina as cotas de sistema padrão que são aplicadas a contas de usuário.                                                                                                                                                                                                                                                                                                   |
| \_segredo de criação de política \_              | Esse tipo de acesso é necessário para criar um novo objeto de dados privado.                                                                                                                                                                                                                                                                                                    |
| \_criar \_ conta de política             | Esse tipo de acesso é necessário para criar um novo objeto de [**conta**](account-object.md) .                                                                                                                                                                                                                                                                               |
| \_requisitos de \_ auditoria do conjunto de políticas \_    | Esse tipo de acesso é necessário para atualizar os requisitos de auditoria do sistema.                                                                                                                                                                                                                                                                                      |
| \_administrador do \_ log de auditoria de política \_           | Esse tipo de acesso é necessário para alterar as características da trilha de auditoria, como seu tamanho máximo ou o período de retenção para registros de auditoria, ou para limpar o log.                                                                                                                                                                                               |
| \_informações de \_ auditoria de exibição de política \_    | Esse tipo de acesso é necessário para exibir informações de requisitos de auditoria ou trilha de auditoria.                                                                                                                                                                                                                                                                                  |
| \_administrador do servidor de políticas \_               | Esse tipo de acesso é necessário para modificar as informações de estado do servidor ou função (mestre/réplica). Também é necessário alterar as informações de origem e nome da conta da réplica.                                                                                                                                                                                           |
| \_nomes de pesquisa de política \_               | Esse tipo de acesso é necessário para a conversão entre nomes e SIDs.                                                                                                                                                                                                                                                                                                    |
| \_privilégio de criação de política \_           | Ainda não tem suporte.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Máscaras de acesso genérico

O objeto de [**política**](policy-object.md) publica os seguintes mapeamentos de tipos de acesso genéricos para tipos de acesso específicos:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a>Tipos de acesso padrão

Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE. Todos os tipos de acesso necessários têm suporte. A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é:

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
