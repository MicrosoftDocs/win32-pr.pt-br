---
description: As trocas são inerentes à imposição de segurança.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Decidindo onde impor a segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c13bb81a74b329c662370f24db51559c9dd83f0c1c521ba70dfdcb8be1c813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128759"
---
# <a name="deciding-where-to-enforce-security"></a>Decidindo onde impor a segurança

As trocas são inerentes à imposição de segurança. Um banco de dados pode ser um local natural para colocar a lógica de segurança, considerando que, em última análise, esses dados são a coisa mais importante a ser protegida. No entanto, fazer isso tem implicações significativas de desempenho. Impor a segurança no banco de dados pode ser muito caro, ser dimensionado incorretamente e ser flexível.

## <a name="enforcing-security-in-the-middle-tier"></a>Impor a segurança na camada intermediária

A regra geral a ser seguida com aplicativos escalonáveis de várias camadas usando COM+ é que, sempre que possível, você deve impor segurança detalhada no aplicativo COM+ na camada intermediária. Isso permite que você aproveite totalmente os serviços escalonáveis fornecidos pelo COM+. Impor a autenticação no banco de dados somente quando você precisar e avaliar totalmente as implicações de desempenho de fazer isso.

A situação ideal é poder proteger tabelas de banco de dados para que o aplicativo COM+ possa acessá-las em sua própria identidade. O banco de dados deve apenas autenticar o aplicativo COM+ e confiar nele para autenticar corretamente e autorizar clientes que acessarão dados. Os benefícios dessa abordagem são os seguinte:

-   Ele permite o pool de conexões entre todos os clientes, pois as conexões são completamente genéricas.
-   Geralmente, ele otimiza o acesso a dados, geralmente um ponto problemático ao dimensionar aplicativos.
-   Ele pode minimizar a sobrecarga lógica para impor a segurança, especialmente se a segurança declarativa baseada em função puder ser usada.
-   Ele pode fornecer grande flexibilidade em uma política de segurança. Você pode configurá-lo e [reconfigurá-lo](role-based-security-administration.md)facilmente, conforme descrito em Administração de Segurança Baseada em Função .

Mas, conforme discutido em [Designando](designing-roles-effectively.md)funções com eficiência, embora as funções possam ser aplicadas de maneira fácil e eficaz a algumas relações de dados do usuário, elas não são uma solução universal para decisões de acesso à segurança.

## <a name="enforcing-security-at-the-database"></a>Impor a segurança no banco de dados

Apesar da preferibilidade de impor a segurança na camada intermediária, há vários motivos para impor a segurança no banco de dados, como o seguinte:

-   Você não tem uma opção, talvez por motivos herdado ou talvez porque a decisão simplesmente não está em suas mãos.
-   O banco de dados é acessado por uma ampla variedade de aplicativos e sua segurança não pode ser configurada com base em um único aplicativo.
-   Um banco de dados pode ser protegido de forma previsível. Se você manter dados críticos para a empresa em um banco de dados, poderá desenhar um carrinho rígido em torno dele e ajudar a controlar quem poderá vê-los.
-   A autenticação de clientes originais no banco de dados permite o registro em log detalhado de quem fez o que no banco de dados.
-   Alguns dados são inatamente vinculados a usuários específicos e a lógica de tomar decisões de acesso extremamente finas pode ser executada com mais eficiência no próprio banco de dados, próximo aos dados.

Quando você tem o luxo de projetar a segurança do banco de dados e do aplicativo COM+ em si, a maioria desses problemas pertence às características dos dados em si e sua relação com os usuários que os acessam. Com os dados que podem ser acessados por categorias previsíveis de usuários, é eficiente controlar o acesso na camada intermediária usando funções. Com os dados que são vinculados intricamente a classes muito pequenas de usuários, essas relações geralmente devem ser expressas com os dados em si e, portanto, você deve impor alguma segurança no banco de dados.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Implicações de desempenho da imposição de segurança no banco de dados

Se você autenticar ou autorizar usuários no banco de dados, a identidade do usuário precisará ser propagada para o banco de dados para dar suporte a isso. Se o banco de dados confiar no aplicativo de camada intermediária para fazer isso, será possível passar informações de segurança do usuário em parâmetros. Caso contrário, a chamada para o banco de dados deve ser feita sob a identidade do usuário, o que significa que o aplicativo do servidor deve representar o cliente. Isso pode ter implicações de desempenho, como as seguintes:

-   Representar o cliente pode ser muito mais lento do que fazer a chamada diretamente sob a identidade do aplicativo. Para obter mais detalhes, consulte [Representação e delegação do cliente.](client-impersonation-and-delegation.md)
-   Uma conexão de banco de dados feita em uma identidade de usuário específica não pode ser em pool.
-   A adição de lógica no próprio banco de dados corre o risco de criar um gargalo de dimensionamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cenários básicos para proteger dados em aplicativos de várias camadas](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> </dl>

 

 



