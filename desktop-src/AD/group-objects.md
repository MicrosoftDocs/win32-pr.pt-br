---
title: Agrupar objetos
description: Um grupo é representado como um objeto de grupo no Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a935d2a44d3350d8c24ca3bdb388f0a4bd8f16ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917125"
---
# <a name="group-objects"></a>Agrupar objetos

Um grupo é representado como um objeto de [**grupo**](/windows/desktop/ADSchema/c-group) no Active Directory Domain Services. A tabela a seguir lista atributos importantes do objeto de **grupo** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cn</strong></td>
<td>O <strong>CN</strong> (ou nome comum) é um atributo de valor único que é o nome distinto relativo do objeto. O <strong>CN</strong> é o nome do grupo em Active Directory Domain Services. Assim como acontece com todos os outros objetos, o <strong>CN</strong> de um grupo deve ser exclusivo entre os objetos irmãos no contêiner que contém o grupo.<br/></td>
</tr>
<tr class="even">
<td><strong>associado</strong></td>
<td>O atributo <strong>Member</strong> é um atributo com vários valores que contém a lista de nomes distintos para os objetos User, Group e Contact que são membros do grupo. Cada item na lista é uma referência vinculada ao objeto que representa o membro; Portanto, o servidor de Active Directory atualiza automaticamente os nomes distintos na Propriedade Member quando um objeto member é movido ou renomeado.<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td>O atributo <strong>GroupType</strong> é um atributo de valor único que é um inteiro que especifica o tipo de grupo e o escopo usando os seguintes sinalizadores de bits:
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> Os três primeiros sinalizadores especificam o escopo do grupo. O sinalizador <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> indica o tipo de grupo. Se esse sinalizador for definido, o grupo será um grupo de segurança. Se esse sinalizador não for definido, o grupo será um grupo de distribuição. Para obter mais informações, consulte <a href="#group-types">tipos de grupo</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td>O atributo <strong>memberOf</strong> é um atributo de vários valores que contém a lista de nomes distintos para grupos que contêm o grupo como um membro. Esse atributo lista os grupos abaixo dos quais o grupo é aninhado diretamente não contém a lista recursiva de predecessores aninhados. Por exemplo, se o grupo D fosse aninhado no grupo C e o grupo b e o grupo B fossem aninhados no grupo A, o atributo <strong>memberOf</strong> do Grupo D listaria o grupo C e o grupo b, mas não o grupo a.<br/></td>
</tr>
<tr class="odd">
<td><strong>objectGUID</strong></td>
<td>O atributo <strong>objectGUID</strong> é um atributo de valor único que é o identificador exclusivo do objeto. Esse atributo é um GUID (identificador global exclusivo). Quando um objeto é criado no diretório, o servidor de Active Directory gera um GUID e o atribui ao atributo <strong>objectGUID</strong> do objeto. O GUID é exclusivo em toda a empresa e em qualquer outro lugar.<br/> O <strong>objectGUID</strong> é uma estrutura de GUID de 128 bits armazenada como um octetostring.<br/></td>
</tr>
<tr class="even">
<td><strong>objectSid</strong></td>
<td>O atributo <strong>objectSid</strong> é um atributo de valor único que especifica o Sid (identificador de segurança) do grupo. O SID é um valor exclusivo usado para identificar o grupo como uma entidade de segurança. É um valor binário que o sistema define quando o grupo é criado.<br/> Cada grupo tem um SID exclusivo que o domínio do Windows NT/Windows 2000 Server emite, que é armazenado no atributo <strong>objectSid</strong> do objeto de grupo no diretório. Cada vez que um usuário faz logon, o sistema recupera o SID para os grupos dos quais o usuário é membro e o coloca no token de acesso do usuário. O sistema usa os SIDs no token de acesso do usuário para identificar o usuário e suas associações de grupo em todas as interações subsequentes com a segurança do Windows NT/Windows 2000.<br/> Quando um SID é usado como o identificador exclusivo para um usuário ou grupo, ele não pode nunca ser usado novamente para identificar outro usuário ou grupo.<br/></td>
</tr>
<tr class="odd">
<td><strong>sAMAccountName</strong></td>
<td>O atributo <strong>sAMAccountName</strong> é um atributo de valor único que é o nome de logon usado para dar suporte a clientes e servidores de uma versão anterior (Windows 95, Windows 98 e LAN Manager). O <strong>sAMAccountName</strong> deve ter menos de 20 caracteres para dar suporte a clientes e servidores de uma versão anterior.<br/> O <strong>sAMAccountName</strong> deve ser exclusivo entre todos os objetos de entidade de segurança em um domínio.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>Tipos de grupo

Há dois tipos de grupos definidos por Active Directory Domain Services, *grupos de segurança* e *grupos de distribuição*.

Um grupo de segurança fornece um agrupamento lógico de objetos e o próprio grupo pode ser usado como uma entidade de segurança em uma ACL (lista de controle de acesso). Quando um grupo de segurança recebe acesso a um objeto, todos os membros do grupo de segurança recebem automaticamente o mesmo acesso ao objeto. Os grupos de segurança com escopo universal também podem ser usados como uma entidade de email. Enviar uma mensagem de email para um grupo de segurança universal envia a mensagem a todos os membros do grupo.

Um grupo de distribuição também fornece um agrupamento lógico de objetos, mas não pode fornecer nenhum privilégio de acesso. Os grupos de distribuição não estão habilitados para segurança e não podem ser usados como uma entidade de segurança em uma ACL. Os grupos de distribuição são usados somente para fins de agrupamento. Por exemplo, as listas de distribuição podem ser usadas com aplicativos de email, como o Exchange, para enviar emails a uma coleção de usuários.

Para obter mais informações sobre tipos de grupo no Active Directory Domain Services, consulte o tópico [tipos de grupo](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) no [Microsoft TechNet](https://technet.microsoft.com/default.aspx).

## <a name="group-scope"></a>Escopo do Grupo

Há três escopos de grupo que são definidos por Active Directory Domain Services, *Universal*, *global* e *domínio local*. O escopo do grupo define quais tipos de objeto podem pertencer ao grupo, a quais tipos de grupos o grupo pode ser membro e o escopo dos objetos aos quais os grupos de segurança podem receber acesso. Quando o nível funcional do domínio é definido como modo misto do Windows 2000, os grupos de segurança com escopo universal não podem ser criados.

A tabela a seguir lista os três escopos de grupo e mais informações sobre cada escopo para um grupo de segurança.

| Escopo                   | Membros possíveis                                                                                                                                                                                                                                      | Conversão de escopo                                                                                                                                                 | Pode conceder permissões                                                       | Possível membro de                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universal<br/>    | Contas de qualquer domínio na mesma floresta.<br/> Grupos globais de qualquer domínio na mesma floresta.<br/> Outros grupos universais de qualquer domínio na mesma floresta.<br/>                                                            | Pode ser convertido em escopo de domínio local.<br/> Pode ser convertido em escopo global desde que o grupo não contenha outros grupos universais.<br/> | Em qualquer domínio na mesma floresta ou em florestas confiantes.<br/>            | Outros grupos universais na mesma floresta.<br/> Grupos locais de domínio na mesma floresta ou em florestas confiantes.<br/> Grupos locais em computadores na mesma floresta ou em florestas confiantes.<br/>            |
| Global<br/>       | Contas do mesmo domínio.<br/> Outros grupos globais do mesmo domínio.<br/>                                                                                                                                                        | Pode ser convertido para o escopo universal, contanto que o grupo não seja membro de nenhum outro grupo global.<br/>                                                   | Em qualquer domínio na mesma floresta ou em domínios ou florestas confiantes.<br/> | Grupos universais de qualquer domínio na mesma floresta.<br/> Outros grupos globais do mesmo domínio.<br/> Grupos locais de domínio de qualquer domínio na mesma floresta ou de qualquer domínio confiante.<br/> |
| Domínio local<br/> | Contas de qualquer domínio ou domínio confiável.<br/> Grupos globais de qualquer domínio ou domínio confiável.<br/> Grupos universais de qualquer domínio na mesma floresta.<br/> Outros grupos locais de domínio do mesmo domínio.<br/> | Pode ser convertido para o escopo universal, contanto que o grupo não contenha outros grupos locais de domínio.<br/>                                              | Dentro do mesmo domínio.<br/>                                          | Outros grupos locais de domínio do mesmo domínio.<br/> Grupos locais em computadores no mesmo domínio, excluindo grupos internos que têm SIDs bem conhecidos.<br/>                                             |



 

 

