---
title: Implementando provedores de interfaces de serviço Active Directory
description: As interfaces de serviço do Active Directory (ADSI) são interfaces COM que encapsulam objetos de serviço de diretório para expô-los aos clientes dos serviços de diretório. Ao fornecer uma implementação do ADSI, você expande sua base de clientes para o conjunto de aplicativos cliente ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementando Active Directory ADSI de provedores de interfaces de serviço
- Implementando ADSI de provedores ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634873"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implementando provedores de interfaces de serviço Active Directory

As interfaces de serviço do Active Directory (ADSI) são interfaces COM que encapsulam objetos de serviço de diretório para expô-los aos clientes dos serviços de diretório. Ao fornecer uma implementação do ADSI, você expande sua base de clientes para o conjunto de aplicativos cliente ADSI.

Assim como acontece com qualquer implementação de COM, você pode escrever um provedor ADSI em vários idiomas. As interfaces COM do ADSI são definidas como interfaces duplas que permitem a resolução de nomes em tempo de execução e de compilação e podem ser chamadas por linguagens em conformidade com a automação, como Visual Basic, Visual Basic Scripting Edition, e também as linguagens mais conscientes de desempenho e eficiência, como C e C++. Os clientes ADSI também incluem aplicativos Web que usam Active Server páginas e snap-ins de administração por meio do console de gerenciamento Microsoft.

Como a ADSI fornece seu próprio provedor de OLE DB, a implementação dos recursos de pesquisa definidos pelo [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) também permite que os clientes ADSI consultem os dados do serviço de diretório.

Todos os objetos de serviço de diretório podem ser representados por meio de um objeto ADSI genérico com suporte a [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). A ADSI fornece os blocos de construção necessários para representar os recursos e serviços de qualquer serviço de diretório.

Além disso, as metainterfaces ADSI representam objetos comuns usados por administradores de diretório. Você mapeia as propriedades das metainterfaces para as propriedades com suporte no serviço de diretório. Os clientes ADSI que programam para as interfaces do serviço de Active Directory têm acesso ao serviço de diretório assim que o provedor é instalado e o sistema é reiniciado.

Se o serviço de diretório oferecer suporte a uma representação de esquema, o suporte às interfaces de gerenciamento de esquema tornará seu namespace diretamente acessível aos navegadores do serviço de diretório. Ao publicar seus recursos por meio do esquema, os clientes podem consultar seu serviço de diretório online e aproveitar os serviços que você oferece. Devido à disponibilidade do esquema online e à vantagem da interface COM, você pode continuar disponibilizando novos recursos para o software cliente ao mesmo tempo em que oferece suporte a versões de nível inferior.

 

 




