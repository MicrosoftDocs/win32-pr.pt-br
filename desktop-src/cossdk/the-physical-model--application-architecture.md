---
description: Depois que os modelos conceitual e lógico estiverem concluídos, você poderá tomar decisões sobre a implementação física do aplicativo.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'O modelo físico: arquitetura de aplicativo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089567"
---
# <a name="the-physical-model-application-architecture"></a>O modelo físico: arquitetura de aplicativo

Depois que os modelos conceitual e lógico estiverem concluídos, você poderá tomar decisões sobre a implementação física do aplicativo. Para criar o modelo físico, você deve entender onde os vários serviços do aplicativo devem ser localizados e como eles devem ser implementados. Determinar onde os vários serviços residem deve vir antes de como os serviços serão implementados.

Uma regra básica para determinar onde residem vários serviços é: colocar o componente onde ele está sendo usado. Se, por exemplo, um componente Exibir informações para o cliente base, ele deverá ir para o computador do usuário. Se um componente validar as informações do cliente base, ele também deverá residir no computador do cliente base. Se um componente atualizar as informações em um banco de dados, ele deverá residir no servidor de banco de dados.

Há, é claro, considerações adicionais que fazem exceções a essa regra. Problemas de desempenho e segurança também podem ditar onde um componente está localizado. Considere o seguinte:

-   Um componente passará a ser alterado com frequência, dificultando a distribuição de atualizações?
-   O componente será usado por outros aplicativos, como um componente de verificação de segurança comum?
-   O componente faz cálculos longos ou executa funções, como impressão, que podem ser descarregadas em um servidor?
-   A segurança de um componente pode ser aprimorada colocando-o em um servidor?

Localizar corretamente os componentes de um aplicativo também pode isolar a equipe de desenvolvimento da recodificação dispendiosa se o sistema ou o local dos dados for alterado. Por exemplo, ao colocar as regras de acesso a dados em uma camada de dados em vez de em procedimentos armazenados, o aplicativo é mais facilmente isolado da dependência em um DBMS específico. Não apenas as alterações são refinadas e testadas, mas as fontes de dados podem ser alteradas e os dados podem ser distribuídos sem alterar fundamentalmente o aplicativo.

Por fim, a localização de componentes deve aproveitar as eficiências do sistema. É hora e econômico posicionar objetos comerciais em locais centralizados na rede. Os objetos podem ser compartilhados entre aplicativos e o teste de unidade pode ser feito antes de qualquer componente ser implantado. Os custos de manutenção também podem ser reduzidos porque as alterações de regra ocorrem apenas em um único ponto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo conceitual: requisitos de aplicativo](the-conceptual-model--application-requirements.md)
</dt> <dt>

[O modelo lógico: definição e planejamento de aplicativos](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



