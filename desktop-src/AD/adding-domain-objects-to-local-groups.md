---
title: Adicionando objetos de domínio a grupos locais
description: Os usuários e grupos que pertencem ao domínio podem ser adicionados a grupos no computador local para conceder direitos ao usuário ou grupo de domínio nesse computador específico.
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, adicionando objetos de domínio a grupos locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e956d1cf076f4c33c46700e52798463b7e1d2c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640440"
---
# <a name="adding-domain-objects-to-local-groups"></a>Adicionando objetos de domínio a grupos locais

Quando um servidor membro ou um computador que executa o Windows 2000 Professional é membro de um domínio do Windows 2000, os usuários e grupos que pertencem ao domínio podem ser adicionados a grupos no computador local para conceder direitos ao usuário ou grupo de domínio nesse computador específico.

Ao gerenciar grupos locais de domínio em um domínio do Windows 2000 usando ADSI, o provedor LDAP é normalmente usado. No entanto, ao gerenciar grupos locais em servidores membro e em um computador executando o Windows 2000 Professional, o provedor WinNT deve ser usado.

Somente grupos locais podem ser criados em servidores membros e no Windows 2000 Professional. No entanto, os grupos locais podem conter:

-   Grupos universais e globais da floresta que contêm o domínio do qual o computador é membro.
-   Grupos locais de domínio desse domínio de computador.
-   Usuários de qualquer domínio na floresta.

**Para adicionar um objeto de domínio a um grupo local**

1.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) do computador que contém o grupo local ao qual adicionar um membro. A associação deve ser executada usando uma conta que tenha direitos suficientes para acessar esse computador. A cadeia de vinculação deve assumir o formato "WinNT:// <computer name> , Computer", em que " &lt; Computer name &gt; " é o nome do grupo de computadores ao qual adicionar um membro. O parâmetro ", Computer" instrui a ADSI que ela está vinculando a um computador. A ADSI expõe esses dados ao analisador do provedor de WinNT para que ele possa ignorar algumas consultas de resolução de ambiguidades para determinar o tipo de objeto ao qual você está ligando. Isso pode poupar ao usuário uma espera de 5 a 20 segundos para que a ambiguidade seja resolvida.
2.  Use o método [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) com "Group" como a classe e o nome do grupo local como o nome do objeto a ser associado ao grupo.
3.  Associe à interface [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup) do grupo local ao qual um membro será adicionado.
4.  Construa o ADsPath do objeto para adicionar ao grupo local no formato "Winnt:// <domain> / <name> ", em que " &lt; Domain &gt; " é o nome do domínio que contém o objeto a ser adicionado e " &lt; name &gt; " é o nome do objeto a ser adicionado.
5.  Adicione o usuário ou grupo ao grupo local com o método [**IADs. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) , passando o ADsPath construído na etapa 4.

Para obter mais informações e um exemplo de código que mostra como adicionar um usuário de domínio ou um objeto de grupo a um grupo local, consulte [código de exemplo para adicionar um usuário ou grupo de domínio a um grupo local](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md).

 

 