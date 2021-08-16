---
description: A finalidade da regra de política de autorização central (CAPR) é fornecer uma definição de todo o domínio de um aspecto isolado da política de autorização de organizações.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regra de política de autorização central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5638633f655794464a9d603e1bb6a0380d2224170b9afe0f6314b1f8fee945b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783200"
---
# <a name="central-authorization-policy-rule"></a>Regra de política de autorização central

A finalidade da regra de política de autorização central (CAPR) é fornecer uma definição de todo o domínio de um aspecto isolado da política de autorização da organização. O administrador define o CAPR para impor um dos requisitos de autorização específicos. Como o CAPR define apenas um requisito específico desejado da política de autorização, ele pode ser mais simplesmente definido e compreendido do que se todos os requisitos da diretiva de autorização da organização forem compilados em uma única definição de política.

O CAPR tem os seguintes atributos:

-   Nome – identifica o CAPR para os administradores.
-   Descrição – define a finalidade do CAPR e quaisquer informações que possam ser necessárias para os consumidores do CAPR.
-   Expressão de aplicabilidade – define os recursos ou situações em que a política será aplicada.
-   ID – identificador para uso na auditoria de alterações no CAPR.
-   política de controle de acesso eficaz – um descritor de segurança Windows que contém uma DACL que define a política de autorização efetiva.
-   Expressão de exceção – uma ou mais expressões que fornecem um meio de substituir a política e conceder acesso a uma entidade de segurança de acordo com a avaliação da expressão.
-   política de preparo – um descritor de segurança Windows opcional que contém uma DACL que define uma política de autorização proposta (lista de entradas de controle de acesso) que será testada em relação à política efetiva, mas não imposta. Se houver uma diferença entre os resultados da política efetiva e a política de preparo, a diferença será registrada no log de eventos de auditoria.
    -   Como o preparo pode ter um efeito imprevisível no desempenho do sistema, um administrador de Política de Grupo deve ser capaz de selecionar computadores específicos nos quais o preparo estará em vigor. Isso permite que a política existente esteja em vigor na maioria das máquinas de uma UO enquanto o preparo está acontecendo em um subconjunto dos computadores.
    -   P2 – um administrador local em um determinado computador deve ser capaz de desabilitar o preparo se o preparo nesse computador estiver causando muita degradação do desempenho.
-   Backlink a CAP – uma lista de backlinks para qualquer CAPs que possa se referir a esse CAPR.

Durante a verificação de acesso, o CAPR é avaliado para aplicabilidade com base na expressão de aplicabilidade. Se um CAPR for aplicável, ele será avaliado para determinar se ele fornece ao usuário solicitante o acesso solicitado ao recurso identificado. Os resultados da avaliação de CAPE são logicamente Unidos por **e** com os resultados da DACL no recurso e qualquer outro CAPRs aplicável em vigor no recurso.

Exemplo de CAPRs:

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a>Negar ACEs em CAPEs

em Windows 8 ACEs deny não terão suporte em um CAPR. O UX de criação do CAPR não permitirá a criação de uma ACE Deny. Além disso, quando a LSA recupera o limite de Active Directory, a LSA verificará se nenhum CAPRs tem ACEs Deny. Se uma ACE Deny for encontrada em um CAPR, a CAP será tratada como inválida e não será copiada para o registro ou SRM.

> [!Note]  
> A verificação de acesso não impedirá que nenhuma Ace Deny esteja presente. As ACEs Deny em um CAPR serão aplicadas. Espera-se que as ferramentas de criação impeçam que isso aconteça.

 

## <a name="cape-definition"></a>Definição de cabo

CAPRs são criados por meio de uma nova UX fornecida no Centro Administrativo do Active Directory (ADAC.) No ADAC, uma opção de nova tarefa é fornecida para criar um CAPR. Quando essa tarefa for selecionada, o ADAC solicitará ao usuário uma caixa de diálogo solicitando ao usuário um nome de CAPR e uma descrição. Quando eles são fornecidos, os controles para definir qualquer um dos elementos CAPR restantes são habilitados. Para cada um dos elementos CAPR restantes, o UX chamará a interface do usuário ACL para permitir a definição de expressões e/ou ACLs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Cenário de controle de acesso dinâmico (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
