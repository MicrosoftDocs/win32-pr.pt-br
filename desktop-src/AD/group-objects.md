---
title: Objetos de grupo
description: Um grupo é representado como um objeto de grupo no Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15de5c1577e6c4b0ca738c0f17ea5453020987d9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469933"
---
# <a name="group-objects"></a>Objetos de grupo

Um grupo é representado como um [**objeto de**](/windows/desktop/ADSchema/c-group) grupo em Active Directory Domain Services. A tabela a seguir lista atributos importantes do **objeto de** grupo.




| Atributo | Descrição | 
|-----------|-------------|
| <strong>Cn</strong> | O <strong>cn</strong> (ou Common-Name) é um atributo de valor único que é o nome diferenciado relativo do objeto. O <strong>cn</strong> é o nome do grupo em Active Directory Domain Services. Assim como com todos os outros objetos, o <strong>cn</strong> de um grupo deve ser exclusivo entre os objetos irmãos no contêiner que contém o grupo.<br /> | 
| <strong>Membro</strong> | O <strong>atributo</strong> membro é um atributo de vários valores que contém a lista de nomes diferenciados para os objetos de usuário, grupo e contato que são membros do grupo. Cada item na lista é uma referência vinculada ao objeto que representa o membro; portanto, o servidor do Active Directory atualiza automaticamente os nomes diferenciados na propriedade membro quando um objeto membro é movido ou renomeado.<br /> | 
| <strong>groupType</strong> | O <strong>atributo groupType</strong> é um atributo de valor único que é um inteiro que especifica o tipo de grupo e o escopo usando os seguintes sinalizadores de bit:<ul><li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li></ul><br /> Os três primeiros sinalizadores especificam o escopo do grupo. O <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> sinalizador indica o tipo de grupo. Se esse sinalizador estiver definido, o grupo será um grupo de segurança. Se esse sinalizador não estiver definido, o grupo será um grupo de distribuição. Para obter mais informações, consulte <a href="#group-types">Tipos de grupo</a>.<br /> | 
| <strong>memberOf</strong> | O <strong>atributo memberOf</strong> é um atributo de vários valores que contém a lista de nomes diferenciados para grupos que contêm o grupo como um membro. Esse atributo lista os grupos abaixo dos quais o grupo está diretamente aninhado, ele não contém a lista recursiva de antecessores aninhados. Por exemplo, se o grupo D estivesse aninhado no grupo C e os grupos B e B fossem aninhados no grupo A, o atributo <strong>memberOf</strong> do grupo D listaria o grupo C e o grupo B, mas não o grupo A.<br /> | 
| <strong>Objectguid</strong> | O <strong>atributo objectGUID</strong> é um atributo de valor único que é o identificador exclusivo do objeto. Esse atributo é um GUID (Identificador Global Exclusivo). Quando um objeto é criado no diretório, o servidor do Active Directory gera um GUID e o atribui ao atributo <strong>objectGUID do</strong> objeto. O GUID é exclusivo em toda a empresa e em qualquer outro lugar.<br /> O <strong>objectGUID</strong> é uma estrutura GUID de 128 bits armazenada como um OctetString.<br /> | 
| <strong>Objectsid</strong> | O <strong>atributo objectSid</strong> é um atributo de valor único que especifica o SID (identificador de segurança) do grupo. O SID é um valor exclusivo usado para identificar o grupo como uma entidade de segurança. É um valor binário que o sistema define quando o grupo é criado.<br /> Cada grupo tem um SID exclusivo que o Windows NT/Windows 2000 Server que está armazenado no atributo <strong>objectSid</strong> do objeto de grupo no diretório. Sempre que um usuário faz login, o sistema recupera o SID dos grupos dos quais o usuário é membro e o coloca no token de acesso do usuário. O sistema usa os SIDs no token de acesso do usuário para identificar o usuário e suas associações de grupo em todas as interações subsequentes com a segurança Windows NT/Windows 2000.<br /> Quando um SID tiver sido usado como o identificador exclusivo de um usuário ou grupo, ele não poderá ser usado novamente para identificar outro usuário ou grupo.<br /> | 
| <strong>Samaccountname</strong> | O <strong>atributo sAMAccountName</strong> é um atributo de valor único que é o nome de logon usado para dar suporte a clientes e servidores de uma versão anterior (Windows 95, Windows 98 e LAN Manager). O <strong>sAMAccountName</strong> deve ter menos de 20 caracteres para dar suporte a clientes e servidores de uma versão anterior.<br /> O <strong>sAMAccountName</strong> deve ser exclusivo entre todos os objetos de entidade de segurança dentro de um domínio.<br /> | 




 

## <a name="group-types"></a>Tipos de grupo

Há dois tipos de grupos definidos pelo Active Directory Domain Services, Grupos *de Segurança e* Grupos de *Distribuição*.

Um grupo de segurança fornece um grupo lógico de objetos e o próprio grupo pode ser usado como uma entidade de segurança em uma ACL (Lista de Controle de Acesso). Quando um grupo de segurança recebe acesso a um objeto, todos os membros do grupo de segurança recebem automaticamente o mesmo acesso ao objeto. Grupos de segurança com escopo Universal também podem ser usados como uma entidade de email. Enviar uma mensagem de email para um grupo de segurança universal envia a mensagem a todos os membros do grupo.

Um grupo de distribuição também fornece um grupo lógico de objetos, mas não pode fornecer privilégios de acesso. Os grupos de distribuição não estão habilitados para segurança e não podem ser usados como uma entidade de segurança em uma ACL. Os grupos de distribuição só são usados para fins de grupo. Por exemplo, listas de distribuição podem ser usadas com aplicativos de email, como Exchange, para enviar email para uma coleção de usuários.

Para obter mais informações sobre tipos de grupo Active Directory Domain Services, consulte [o tópico Tipos de](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) grupo no Microsoft [TechNet](https://technet.microsoft.com/default.aspx).

## <a name="group-scope"></a>Escopo do Grupo

Há três escopos de grupo definidos por Active Directory Domain Services, *Universal,* *Global* e *Local de Domínio.* O escopo do grupo define a quais tipos de objeto podem pertencer ao grupo, a quais tipos de grupos o grupo pode ser membro e o escopo de objetos aos quais os grupos de segurança podem receber acesso. Quando o nível funcional do domínio é definido como Windows modo misto 2000, grupos de segurança com escopo universal não podem ser criados.

A tabela a seguir lista os três escopos de grupo e mais informações sobre cada escopo de um grupo de segurança.

| Escopo                   | Membros possíveis                                                                                                                                                                                                                                      | Conversão de escopo                                                                                                                                                 | Pode conceder permissões                                                       | Possível membro de                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universal<br/>    | Contas de qualquer domínio na mesma floresta.<br/> Grupos globais de qualquer domínio na mesma floresta.<br/> Outros grupos universais de qualquer domínio na mesma floresta.<br/>                                                            | Pode ser convertido no escopo local do domínio.<br/> Pode ser convertido em escopo global, desde que o grupo não contenha outros grupos universais.<br/> | Em qualquer domínio na mesma floresta ou em florestas confiantes.<br/>            | Outros grupos universais na mesma floresta.<br/> Grupos locais de domínio na mesma floresta ou florestas confiantes.<br/> Grupos locais em máquinas na mesma floresta ou em florestas confiantes.<br/>            |
| Global<br/>       | Contas do mesmo domínio.<br/> Outros grupos globais do mesmo domínio.<br/>                                                                                                                                                        | Pode ser convertido em escopo universal, desde que o grupo não seja membro de nenhum outro grupo global.<br/>                                                   | Em qualquer domínio na mesma floresta ou domínios ou florestas confiantes.<br/> | Grupos universais de qualquer domínio na mesma floresta.<br/> Outros grupos globais do mesmo domínio.<br/> Grupos locais de domínio de qualquer domínio na mesma floresta ou de qualquer domínio confiante.<br/> |
| Local do Domínio<br/> | Contas de qualquer domínio ou qualquer domínio confiável.<br/> Grupos globais de qualquer domínio ou qualquer domínio confiável.<br/> Grupos universais de qualquer domínio na mesma floresta.<br/> Outros grupos locais de domínio do mesmo domínio.<br/> | Pode ser convertido em escopo universal, desde que o grupo não contenha nenhum outro grupo local de domínio.<br/>                                              | Dentro do mesmo domínio.<br/>                                          | Outros grupos locais de domínio do mesmo domínio.<br/> Grupos locais em máquinas no mesmo domínio, excluindo grupos integrados que têm SIDs conhecidos.<br/>                                             |



 

 

