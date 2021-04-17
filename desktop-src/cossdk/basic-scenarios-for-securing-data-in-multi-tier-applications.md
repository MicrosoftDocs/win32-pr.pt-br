---
description: Este tópico apresenta alguns cenários de bloco de construção, ilustrando os critérios discutidos em decidindo onde impor a segurança.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Cenários básicos para proteger dados em aplicativos de várias camadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782696"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Cenários básicos para proteger dados em aplicativos de várias camadas

Este tópico apresenta alguns cenários de bloco de construção, ilustrando os critérios discutidos em [decidindo onde impor a segurança](deciding-where-to-enforce-security.md).

## <a name="trusted-server-scenario"></a>Cenário de servidor confiável

-   O banco de dados confia totalmente no aplicativo COM+ para autenticar e autorizar os usuários finais a acessar os dados no banco de dado.
-   Preferivelmente, o banco de dados é protegido contra qualquer acesso, exceto pelo aplicativo.
-   O aplicativo COM+ usa a segurança baseada em função para autorizar usuários.
-   As conexões são abertas sob a identidade do aplicativo COM+ e são totalmente pooling.
-   A auditoria e o registro em log podem ser feitos pelo aplicativo COM+, ou essas informações podem ser passadas para o banco de dados pelo aplicativo.

Esse cenário funciona melhor para dados que podem ser acessados por categorias previsíveis de usuários que podem ser encapsuladas em funções. Por exemplo, somente "gerentes", "informadores" e "contadores" têm permissão para acessar contas. A lógica de negócios do que precisamente cada um está habilitado é imposta na camada intermediária.

## <a name="impersonation-scenario"></a>Cenário de representação

-   O banco de dados faz sua própria autenticação e autorização de usuários finais para ajudar a limitar o acesso a dados no banco de dado.
-   O aplicativo COM+ representa clientes sempre que ele está acessando o banco de dados.
-   As conexões são feitas em uma base por chamada e não podem ser reutilizadas.

Esse cenário funciona melhor para dados que estão fortemente ligados a classes muito pequenas de usuários. Por exemplo, cada funcionário pode acessar apenas seu próprio arquivo de equipe, e cada gerente pode acessar somente os arquivos de equipe de seus relatórios.

## <a name="hybrid-scenario"></a> Cenário Híbrido

Uma combinação dos dois cenários anteriores, em que a representação é usada somente quando necessário.

Esse cenário funciona melhor em situações em que você tem relações de dados de usuário híbridos. Por exemplo, você tem "gerentes", "Digars", "contadores" e milhares de clientes Web individuais que podem acessar apenas suas próprias contas. Você pode separar caminhos lógicos por meio do aplicativo, potencialmente com componentes separados, para lidar com a última classe de usuários, principalmente onde as suposições de desempenho para esses usuários são diferentes.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>Cenário confiável usando funções de Microsoft SQL Server

-   Microsoft SQL Server 7,0 e posterior podem autorizar o acesso a linhas específicas usando funções, mas confia no aplicativo COM+ para autenticar e autorizar usuários e mapeá-los para as funções corretas no banco de dados.
-   O aplicativo COM+ autoriza os usuários usando a segurança baseada em função e as funções de aplicativo correspondem bem às funções de banco de dados.
-   As conexões podem ser abertas que são específicas para uma função de banco de dados específica. Essas conexões podem ser reutilizadas se forem mantidas por objetos em pool nos aplicativos COM+. Para obter detalhes sobre como fazer isso, consulte [pooling de objetos com+](com--object-pooling.md).
-   A auditoria e o registro em log podem ser feitos pelo aplicativo COM+, ou essas informações podem ser passadas para o banco de dados pelo aplicativo.

Esse cenário funciona melhor para geralmente os mesmos tipos de usuários e dados que no primeiro cenário de servidor confiável, pois o aplicativo COM+ ainda é amplamente confiável para lidar com a autorização corretamente. No entanto, ele ajuda a proteger o banco de dados contra acesso não autorizado e, ao mesmo tempo, permite o acesso potencialmente de várias fontes fora do aplicativo COM+, sem incorrer no dimensionamento e nas penalidades de desempenho presentes com o cenário de representação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Decidindo onde impor a segurança](deciding-where-to-enforce-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> </dl>

 

 



