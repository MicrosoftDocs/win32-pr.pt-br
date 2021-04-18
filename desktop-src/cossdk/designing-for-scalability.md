---
description: A escalabilidade é a capacidade de um aplicativo de atender a uma carga adicional com um aumento linear no uso de recursos.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Projetando para escalabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789259"
---
# <a name="designing-for-scalability"></a>Projetando para escalabilidade

A escalabilidade é a capacidade de um aplicativo de atender a uma carga adicional com um aumento linear no uso de recursos. A escalabilidade é importante em qualquer aplicativo distribuído. Os limites de escalabilidade geralmente são centralizados em relação ao uso de recursos e dependências inadvertidamente criadas no design do aplicativo.

A lista a seguir descreve problemas de escalabilidade e sugere soluções:

-   Recursos dentro do computador. O número de threads e a memória disponível pode limitar a escalabilidade. Use um modelo de Threading que seja mais eficiente para seu aplicativo.
-   Recursos entre computadores. O número de computadores disponíveis para distribuir a carga de trabalho do aplicativo pode afetar a escalabilidade.
-   Afinidade de cliente. Duas situações de afinidade podem ser criadas inadvertidamente por um aplicativo: uma situação em que o aplicativo depende do estado dos dados que o cliente envia com sua solicitação; e uma situação em que o aplicativo requer um estado específico do cliente. Evite a criação de dependência de estado entre o cliente e o aplicativo.
-   Afinidade de servidor. Um aplicativo COM+ pode limitar sua escalabilidade criando uma afinidade de servidor, onde o aplicativo depende de ir para um determinado computador servidor para obter informações. Essa afinidade pode ocorrer com muitos aplicativos orientados a banco de dados. A melhor maneira de evitar um afunilamento de afinidade de servidor é particionar dados em vários computadores de servidor. Por exemplo, divida os dados do cliente entre os servidores pela chave acessada com mais frequência ou alcance um banco de dado do cliente em vários servidores usando o sobrenome do cliente (por exemplo, server1: a-f, server2: g-m, Server3: n-z).
    > [!Note]  
    > O particionamento de dados pode adicionar uma grande quantidade de complexidade à lógica de programação e deve ser feito somente depois que outras opções para aumentar a escalabilidade tiverem sido tentadas.

     

-   Tempo de vida do objeto. Para ser escalonável, um aplicativo COM+ deve prestar atenção próxima à vida útil dos objetos. Embora exista um objeto, ele está consumindo recursos. É importante garantir que os tempos de vida de objetos que mantêm os recursos caros sejam gerenciados cuidadosamente. Para objetos de alta demanda que não consomem recursos caros, o [pool de objetos do com+](com--object-pooling.md) pode aumentar a escalabilidade, pois você pode ajustar administrativamente os valores de Pooling para tirar proveito de qualquer hardware que você possa ter. E é uma maneira natural de controlar as conexões: por exemplo, se você tiver uma licença para 20 conexões SQL, poderá ditar isso com a configuração Max pool.
-   Agrupamento de componentes de aplicativos. Para melhorar a escalabilidade de um aplicativo COM+, os componentes de camada intermediária devem ser divididos em serviços dependentes de tempo e independentes de tempo. Isso permite que você se concentre em possivelmente usando um serviço do Microsoft Windows para implementar uma ação de componente necessária. Por exemplo, você pode optar por usar um serviço como o [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) ou [componentes em fila com+](com--queued-components.md) para lidar com tarefas assíncronas independentes de tempo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando para disponibilidade](designing-for-availability.md)
</dt> <dt>

[Projetando para implantação](designing-for-deployment.md)
</dt> <dt>

[Projetando para segurança](designing-for-security.md)
</dt> </dl>

 

 



