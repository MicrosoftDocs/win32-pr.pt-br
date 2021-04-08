---
description: Diretrizes básicas para criar aplicativos COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Diretrizes básicas para criar aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089377"
---
# <a name="basic-guidelines-for-designing-com-applications"></a>Diretrizes básicas para criar aplicativos COM+

Para aproveitar ao máximo o COM+, há algumas diretrizes básicas que você pode usar ao criar um aplicativo:

-   **Modele seu estado durável como um esquema de banco de dados, usando a ferramenta de banco de dados de sua escolha.** Quase todos os aplicativos precisam manter o estado durável. Os bancos de dados fornecem os serviços necessários para criar um armazenamento durável e escalonável do estado. Portanto, a primeira etapa na criação de um aplicativo COM+ é modelar o estado durável de seu aplicativo como um tipo de esquema de banco de dados. Na verdade, não importa qual banco de dados você usa; a maioria dos bancos de dados comerciais é compatível com o COM+. Microsoft SQL Server é um bom exemplo de uma solução que você pode usar.

-   **Modele a lógica do seu aplicativo COM+ como um conjunto de interfaces COM.** Depois que você tiver um esquema que representa as informações de estado do aplicativo, modele as trocas que acontecem no aplicativo como interfaces COM. Essas interfaces modelarão o comportamento do aplicativo. Esse também é o estágio de desenvolvimento quando você deve determinar quais serviços COM+ funcionam melhor para seu aplicativo.

-   **Criar DLLs de componentes que contêm componentes que usam o esquema de dados físicos e expõem uma exibição lógica dos dados para outros componentes (o primeiro item dessa lista), bem como componentes que são implementados em termos do modelo de dados lógicos (o segundo item nessa lista).** Depois de ter a estrutura da lógica e as informações de estado, você pode começar a escrever código e agora pode gravar componentes COM baseados em DLL que implementam as interfaces em termos do esquema definido. Seus componentes simplesmente atuam como manipuladores para trabalhar com suas informações de banco de dados, e as DLLs de componentes permitem criar um aplicativo COM+ que funcione e que seja dimensionado com êxito.

-   **Implante os componentes no ambiente COM+ usando os serviços COM+ que você selecionou.** Depois de criar o aplicativo, você pode implantar o aplicativo em um cluster de rede ou de servidor. Agora você pode tomar decisões com base nos recursos disponíveis e pode personalizar cada componente para obter o máximo de desempenho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Princípios e pressuposições de design de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Criando o aplicativo COM+ usando UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Dicas de design gerais para usar o COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Otimizando interações com a camada de lógica de negócios do COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Outras ferramentas da Microsoft para a criação de aplicativos distribuídos](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



