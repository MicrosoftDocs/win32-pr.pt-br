---
description: Acessando o catálogo COM+
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Acessando o catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de7c87da1744e23b384199dce68628fd77d5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105800063"
---
# <a name="accessing-the-com-catalog"></a>Acessando o catálogo COM+

O catálogo COM+ é o armazenamento de dados subjacente que contém todos os dados de configuração do COM+. Sempre que você fizer qualquer tipo de administração COM+, você está lendo e gravando dados armazenados no catálogo. A única maneira de poder acessar o catálogo é por meio da ferramenta administrativa serviços de componentes ou da biblioteca COMAdmin.

O catálogo COM+ fornece uma camada de abstração sobre os detalhes reais de onde e como os dados de configuração do COM+ são armazenados. Grande parte dos dados é armazenada no banco de dados de registro do COM+ (ou RegDB), que contém dados para todos os componentes configurados instalados em aplicativos COM+. Esse banco de dados é usado no tempo de execução de um aplicativo para fornecer a um objeto de configuração para o COM+ ativar corretamente objetos em um contexto apropriado, permitindo que os serviços sejam fornecidos para objetos por sua configuração. O próprio RegDB é um Gerenciador de recursos transacionado que usa transações do DTC por meio do [Gerenciador de recursos de compensação](com--compensating-resource-manager.md); Quando você faz alterações de configuração persistentes, elas são confirmadas de forma transacional. A única maneira de poder acessar o RegDB é por meio do catálogo COM+, usando os objetos COMAdmin ou a ferramenta administrativa serviços de componentes.

Em cada computador, há um servidor de catálogo COM+ em execução como um componente no aplicativo do sistema. O servidor de catálogo controla o acesso aos dados de catálogo armazenados em seu computador; na verdade, o servidor de catálogo é um mecanismo de consulta que permite que você leia e grave dados no catálogo nesse computador. Quando você inicia a administração programática instanciando um objeto [**COMAdminCatalog**](comadmincatalog.md) , esse objeto abre uma sessão com o servidor de catálogo local. As solicitações de coleções ou itens de coleção no catálogo local são manipuladas pelo servidor de catálogo local. Ao se conectar a um computador remoto, você está se comunicando com o servidor de catálogo nesse computador.

## <a name="security-considerations-in-administration"></a>Considerações de segurança na administração

Para alterar os dados no catálogo COM+, você precisa ter autoridade como administrador. Para usar a ferramenta administrativa serviços de componentes para alterar quaisquer dados de configuração, você precisa ser um membro da função Administradores atribuída ao aplicativo do sistema no computador que você está tentando administrar. Da mesma forma, para alterar todos os dados usando os objetos COMAdmin, seu código precisa estar em execução com a autoridade de administrador. Ou seja, um aplicativo ou script que usa os objetos COMAdmin deve ser executado sob uma conta de usuário que é atribuída à função Administradores no aplicativo do sistema no computador que está tentando administrar. O aplicativo pode acessar e alterar informações no catálogo somente na medida em que a conta em que ela está sendo executada tem essa autoridade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Descrição resumida das classes COMAdmin](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



