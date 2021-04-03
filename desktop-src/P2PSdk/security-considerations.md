---
description: Este tópico discute considerações de segurança específicas ao usar a infraestrutura de pares.
ms.assetid: 088a2111-f4ee-4bec-98a9-ac138950958b
title: Considerações de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd3078834b3a69f988d17e5cbfd5fa1bd1591e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829331"
---
# <a name="security-considerations"></a>Considerações de segurança

Este tópico discute considerações de segurança específicas ao usar a infraestrutura de pares.

Quando você desenvolve um aplicativo de mesmo nível usando a infraestrutura de mesmo nível, por motivos de segurança, você deve considerar permissões de diretório, acesso de convidado a serviços de rede de mesmo nível, divulgação de informações e implementação do provedor de serviços de segurança.

## <a name="directory-permissions"></a>Permissões de diretório

Os serviços de rede ponto a ponto armazenam dados na árvore de diretório de perfil do usuário de um usuário. Um usuário deve ter permissões de gravação na subárvore de **dados do aplicativo** do perfil. Por padrão, essa ACL (lista de controle de acesso) é definida corretamente, mas um usuário pode alterá-la manualmente.

## <a name="guest-access-to-peer-networking-services"></a>Acesso de convidado aos serviços de rede de mesmo nível

Uma conta de convidado e os membros do grupo de segurança de **convidados** do Windows não têm acesso à maioria dos serviços de mesmo nível. Os aplicativos devem ter acesso de usuário local ou superior.

## <a name="information-disclosure"></a>Divulgação de informações

A divulgação de informações envolve endereço, banco de dados e identidade e credenciais de grupo. As seções a seguir identificam e definem a divulgação de informações.

**Divulgação de endereço** O PNRP (Peer Name Resolution Protocol) é um serviço de resolução de identificador que permite que um identificador de nome de par seja resolvido em um endereço IP. Semelhante ao DNS, o PNRP publica um endereço IP para que os usuários que conhecem o identificador correspondente possam solucioná-lo para esse endereço.

-   A publicação de um identificador em PNRP significa que qualquer usuário pode resolver o identificador para o endereço IP publicado e determinar o endereço IP do serviço PNRP que publicou a identidade.
-   A infraestrutura de agrupamento de pares publica automaticamente o nome do grupo de pares da instância de grupo local em PNRP. Enquanto estiver conectado a um grupo de pares, qualquer pessoa que conheça o nome do par para o grupo pode resolver os endereços de membros ativos e conhecer o endereço atual de cada usuário.

A capacidade de um usuário se conectar a outros membros do grupo de mesmo nível ou a nós de grafo pares enquanto estiver conectado é um recurso principal de rede de mesmo nível. Enquanto estiver conectado a um grupo de pares ou grafo, o endereço IP atual de um usuário poderá ser publicado em um registro de presença dentro do grafo ou do grupo de pares. Por padrão, qualquer pessoa que participa desse grupo de pontos ou grafo pode enumerar membros do grupo ou do grafo e determinar os endereços atuais dos membros. Essa capacidade é um agrupamento de pares e uma propriedade de grafo de pares configuráveis.

**Divulgação de banco de dados** As infraestruturas de agrupamento e gráfico de pares registram bancos de dados armazenados no sistema de arquivos local. Qualquer usuário do Windows com acesso administrativo ao sistema de arquivos local (como um administrador local) pode, teoricamente, acessar os dados no grafo de pares local ou no banco de dados de grupo. Isso é consistente com a capacidade de administradores locais acessarem quaisquer dados no computador local.

**Divulgação de credenciais de grupo e identidade** O agrupamento ponto a ponto exige que os Membros estabeleçam conexões entre si para autenticar usando cadeias de certificados X. 509 modificadas. Como parte da autenticação, as cadeias correspondentes de identidade e GMC (certificado de associação de grupo) de cada membro são trocadas.

Enquanto estiver conectado a um grupo de pares, a infraestrutura de agrupamento de pares publica o nome de par do grupo com o PNRP. Como parte da operação de PNRP normal, a cadeia de GMC para esse grupo pode ser fornecida a outras instâncias de PNRP para provar a autorização para publicar o nome de par do grupo.

## <a name="security-service-provider-implementation"></a>Implementação do provedor de serviços de segurança

A infraestrutura de grafo de pares é tão segura quanto o SSP (provedor de serviços de segurança) que o desenvolvedor de aplicativos implementa. Quanto mais forte for o SSP, mais forte a segurança do aplicativo de grafo de pares.

 

 



