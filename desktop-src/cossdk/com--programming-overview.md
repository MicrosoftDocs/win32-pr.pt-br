---
description: O COM+ fornece um ambiente de desenvolvimento corporativo, baseado no Microsoft Component Object Model (COM), para criar aplicativos distribuídos e baseados em componentes.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Visão geral da programação COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421fd6a52eade351eaab09ececff8fc63cc687002dede350ab9f06fa0b2c20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096886"
---
# <a name="com-programming-overview"></a>Visão geral da programação COM+

O COM+ fornece um ambiente de desenvolvimento corporativo, baseado no Microsoft Component Object Model (COM), para criar aplicativos distribuídos e baseados em componentes. Ele também fornece as ferramentas para criar aplicativos transacionais e de várias camadas. O COM+ combina aprimoramentos ao desenvolvimento tradicional baseado em com com muitos serviços administrativos e de programação úteis. Consulte [serviços com+](com--services.md) para obter uma lista completa desses serviços.

Os aprimoramentos do COM incluem melhorias no Threading e na segurança, juntamente com a introdução dos serviços de sincronização. Os serviços incluem a ferramenta administrativa serviços de componentes.

Para aqueles familiarizados com a programação COM, os aprimoramentos do COM+ são significativos, incluindo o seguinte:

-   O COM+ implementa um modelo de Threading chamado Threading Apartment neutro, que permite que um componente tenha acesso serializado junto com a capacidade de executar em qualquer thread.
-   O COM+ dá suporte a componentes com um ambiente especial chamado de [contexto](com--contexts.md), que fornece um conjunto extensível de propriedades que definem o ambiente de execução para o componente.
-   O COM+ fornece segurança baseada em função, execução de objeto assíncrono e um moniker interno que representa uma referência a uma instância de objeto em execução em um servidor fora do processo.

## <a name="application-and-component-administration"></a>Administração de aplicativos e componentes

No COM+, um banco de dados de registro, chamado RegDB, armazena os metadados que descrevem os componentes. Esse banco de dados é altamente otimizado para o tipo de informações de que o COM+ precisa para a ativação de componentes e é usado em vez do registro do sistema. Além disso, o COM+ expõe o *catálogo com+*, que acessa informações no RegDB. O catálogo COM+ é um armazenamento de dados do sistema que contém informações de configuração para aplicativos COM+ em um determinado computador servidor.

Por fim, a ferramenta administrativa serviços de componentes fornece uma interface de usuário totalmente programável para desenvolvedores e administradores para administrar componentes, bem como para implantar aplicativos multicamadas do lado do cliente e do lado do servidor. Para obter mais informações, consulte [Implantando aplicativos com+](deploying-com--applications.md).

## <a name="automatic-transactions"></a>Transações automáticas

O COM+ dá suporte a toda a semântica do MTS (Microsoft Transaction Server) 2,0 e adiciona a funcionalidade [automática](enabling-auto-done-for-a-method.md) , que pode ser definida usando a ferramenta administrativa serviços de componentes. Esse recurso permite que o sistema anule uma transação automaticamente se uma exceção for disparada ou confirmar se não. Para obter mais informações, consulte [Transações com+](com--transactions.md)e [ativação Just-in-time do com+](com--just-in-time-activation.md).

 

 



