---
description: Outras ferramentas da Microsoft para a criação de aplicativos distribuídos
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Outras ferramentas da Microsoft para a criação de aplicativos distribuídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793345"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Outras ferramentas da Microsoft para a criação de aplicativos distribuídos

Além das ferramentas do COM+, a Microsoft fornece as seguintes ferramentas para ajudar o desenvolvedor na criação de aplicativos distribuídos:

-   MDAC (Microsoft Data Access Components). A Microsoft fornece vários caminhos para recuperar dados de uma infinidade de fontes. Por exemplo, OLE DB oferece um conjunto de interfaces COM para a criação de componentes de banco de dados. As interfaces são definidas para que os provedores de dados possam implementar diferentes níveis de suporte, com base nos recursos do armazenamento de dados subjacente. Como o OLE DB é baseado em COM, ele pode ser facilmente estendido e as extensões são implementadas como novas interfaces. O OLE DB também inclui uma interface de programação de nível de aplicativo, chamada ActiveX Data Objects (ADO). O ADO expõe interfaces duplas, para que possa ser facilmente usado por meio de linguagens de script, bem como Microsoft Visual C++, Visual Basic e outras ferramentas de desenvolvedor.

    > [!Note]  
    > Os desenvolvedores também podem optar por usar uma API genérica, neutra para o fornecedor, como a API (interface de programação de aplicativo) do Microsoft Open Database Connectivity (ODBC). A API ODBC é uma interface de linguagem C para acessar dados em um DBMS usando o linguagem SQL (SQL). Um Gerenciador de driver ODBC fornece a interface de programação e os componentes de tempo de execução para localizar drivers específicos de DBMS. Os drivers ODBC, normalmente fornecidos pelo fornecedor do DBMS, convertem chamadas genéricas do Gerenciador de driver ODBC em chamadas para o método de acesso a dados nativo. A principal vantagem de usar a API ODBC é que você precisa aprender apenas uma API para acessar uma ampla gama de DBMSs.

     

-   Microsoft SQL Server. Além de fornecer um sistema de banco de dados relacional robusto e eloqüência, o Microsoft SQL Server pode fornecer um aplicativo distribuído com o pool de conexões e segurança que podem ser integrados ao modelo de segurança do Windows.

-   Integração de transações COM (COMTI). O COMTI pode ser usado para integrar sistemas de mainframe em sistemas Windows, incluindo aplicativos COM+. O COMTI usa protocolos de comunicação padrão (por exemplo, LU 6,2) para a comunicação entre computadores com Windows e mainframe e minicomputers.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Princípios e pressuposições de design de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Criando o aplicativo COM+ usando UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Dicas de design gerais para usar o COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Otimizando interações com a camada de lógica de negócios do COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



