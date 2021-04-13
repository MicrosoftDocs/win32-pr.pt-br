---
description: As compensações são inerentes à imposição de segurança.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Decidindo onde impor a segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac994fb98d50a7e26f1b8142e77dc9ff771f6b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500852"
---
# <a name="deciding-where-to-enforce-security"></a>Decidindo onde impor a segurança

As compensações são inerentes à imposição de segurança. Um banco de dados pode ser um local natural para colocar a lógica de segurança, Considerando que os dados são a coisa mais importante a ser protegida. No entanto, isso tem implicações de desempenho significativas. A imposição da segurança no banco de dados pode ser muito cara, escala ruim e é inflexível.

## <a name="enforcing-security-in-the-middle-tier"></a>Impondo a segurança na camada intermediária

A regra geral a seguir com aplicativos de várias camadas escalonáveis usando COM+ é que, sempre que possível, você deve impor segurança detalhada no aplicativo COM+ na camada intermediária. Isso permite que você aproveite totalmente os serviços escalonáveis fornecidos pelo COM+. Impor a autenticação no banco de dados somente quando for absolutamente necessário, e avaliar totalmente as implicações de desempenho de fazer isso.

A situação ideal é poder proteger tabelas de banco de dados para que o aplicativo COM+ possa acessá-las em sua própria identidade. O banco de dados deve apenas autenticar o aplicativo COM+ e confiar nele para autenticar e autorizar corretamente os clientes que acessarão os dados. Os benefícios dessa abordagem são os seguintes:

-   Ele habilita o pool de conexões entre todos os clientes, pois as conexões são completamente genéricas.
-   Em geral, ele otimiza o acesso a dados, geralmente um ponto de obstrução problemático durante o dimensionamento de aplicativos.
-   Ele pode minimizar a sobrecarga lógica para impor a segurança, especialmente se a segurança declarativa baseada em função puder ser usada.
-   Ele pode fornecer grande flexibilidade em uma política de segurança. Você pode configurá-lo e reconfigurá-lo facilmente, conforme descrito em [Administração de segurança baseada em funções](role-based-security-administration.md).

Mas, conforme discutido na [criação de funções com eficiência](designing-roles-effectively.md), embora as funções possam ser aplicadas de forma fácil e eficaz a algumas relações de dados de usuário, elas não são uma solução universal para decisões de acesso de segurança.

## <a name="enforcing-security-at-the-database"></a>Impondo a segurança no banco de dados

Apesar da preferência de aplicar a segurança na camada intermediária, há vários motivos para impor a segurança no banco de dados, como o seguinte:

-   Você não tem uma opção, talvez por motivos herdados ou talvez porque a decisão simplesmente não está em suas mãos.
-   O banco de dados é acessado por uma ampla variedade de aplicativos, e sua segurança não pode ser configurada com base em um único aplicativo.
-   Um banco de dados pode ser tornado protegido de forma previsível. Se você mantiver dados críticos da empresa em um banco de dado, poderá desenhar um vagão rígido em torno dele e ajudar a controlar quem pode vê-lo.
-   A autenticação de clientes originais no banco de dados permite o log detalhado de quem fez o que no banco de dados.
-   Alguns dados são vinculados a usuários específicos, e a lógica de fazer decisões de acesso extremamente refinadas pode ser executada com mais eficiência no banco de dados em si, perto dos mesmos.

Quando você tem o luxo de projetar a segurança do banco de dados e o aplicativo do COM+ em tandem, a maioria desses problemas refere-se às características dos próprios dados e à sua relação com os usuários que o acessam. Com os dados que podem ser acessados por categorias previsíveis de usuários, é eficiente controlar o acesso na camada intermediária usando funções. Com os dados que são ligados de forma complexa a classes muito pequenas de usuários, essas relações geralmente devem ser expressas com os dados propriamente ditos e, portanto, você deve impor alguma segurança a ele.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Implicações de desempenho da imposição de segurança no banco de dados

Se você autenticar ou autorizar usuários no banco de dados, a identidade do usuário precisará ser propagada para o banco de dados para dar suporte a isso. Se o banco de dados confiar no aplicativo de camada intermediária para fazer isso, é possível passar informações de segurança de usuário em parâmetros. Caso contrário, a chamada para o banco de dados deve ser feita sob a identidade do usuário, o que significa que o aplicativo do servidor deve representar o cliente. Isso pode ter implicações de desempenho, como as seguintes:

-   A representação do cliente pode ser muito mais lenta do que fazer a chamada diretamente sob a identidade do aplicativo. Para obter mais detalhes, consulte [representação e delegação do cliente](client-impersonation-and-delegation.md).
-   Uma conexão de banco de dados feita sob uma identidade de usuário específica não pode ser agrupada.
-   A adição de lógica no próprio banco de dados executa o risco de criar um afunilamento de dimensionamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cenários básicos para proteger dados em aplicativos de várias camadas](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> </dl>

 

 



