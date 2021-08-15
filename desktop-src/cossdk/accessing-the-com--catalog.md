---
description: Acessando o catálogo COM+
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Acessando o catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f05d85526cb6d82916aa48a49c7f97e581c01b7410530878a7f6e0fc69dac20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129407"
---
# <a name="accessing-the-com-catalog"></a>Acessando o catálogo COM+

O catálogo COM+ é o armazenamento de dados subjacente que contém todos os dados de configuração COM+. Sempre que você faz qualquer tipo de administração COM+, você está lendo e escrevendo dados armazenados no catálogo. A única maneira de acessar o catálogo é por meio da ferramenta administrativa serviços de componentes ou por meio da biblioteca COMAdmin.

O catálogo COM+ fornece uma camada de abstração sobre os detalhes reais de onde e como os dados de configuração COM+ são armazenados. Grande parte dos dados é armazenada no banco de dados de registro COM+ (ou RegDB), que contém dados para todos os componentes configurados instalados em aplicativos COM+. Esse banco de dados é usado no tempo de execução do aplicativo para fornecer dados de configuração ao COM+ para ativar corretamente objetos em um contexto apropriado, permitindo que os serviços sejam fornecidos para objetos de acordo com sua configuração. O RegDB em si é um gerenciador de recursos transacionado que usa transações DTC por meio do [gerenciador de recursos de compensação](com--compensating-resource-manager.md); quando você faz alterações de configuração persistentes, elas são comprometidas transaticamente. A única maneira de acessar o RegDB é por meio do catálogo COM+, usando os objetos COMAdmin ou a ferramenta administrativa serviços de componentes.

Em cada computador, há um servidor de catálogo COM+ em execução como um componente no aplicativo do sistema. O servidor de catálogo controla o acesso aos dados de catálogo armazenados em seu computador; Na verdade, o servidor de catálogo é um mecanismo de consulta que permite que você leia e escreva dados no catálogo nesse computador. Quando você inicia a administração programática instando um objeto [**COMAdminCatalog,**](comadmincatalog.md) esse objeto abre uma sessão com o servidor de catálogo local. As solicitações de coleções ou itens de coleção no catálogo local são manipuladas pelo servidor de catálogo local. Ao se conectar a um computador remoto, você está se comunicando com o servidor de catálogo nesse computador.

## <a name="security-considerations-in-administration"></a>Considerações sobre segurança na administração

Para alterar dados no catálogo COM+, você precisa ter autoridade como administrador. Para usar a ferramenta administrativa serviços de componentes para alterar quaisquer dados de configuração, você precisa ser um membro da função Administradores atribuída ao aplicativo do sistema no computador que você está tentando administrar. Da mesma forma, para alterar todos os dados usando os objetos COMAdmin, seu código precisa estar em execução com a autoridade de administrador. Ou seja, um aplicativo ou script usando os objetos COMAdmin deve estar em execução em uma conta de usuário atribuída à função Administradores no aplicativo do sistema no computador que está tentando administrar. O aplicativo pode acessar e alterar informações no catálogo apenas na medida em que a conta na qual ele está em execução tem essa autoridade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Descrição resumida das classes COMAdmin](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



