---
title: Objetos de interfaces de serviço do Active Directory
description: O modelo de objeto ADSI consiste em objetos COM. Os clientes manipulam objetos com interfaces. Os provedores ADSI implementam os objetos e suas interfaces.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- ADSI de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20d75454b840597e1fd2ac0599d72d04acb1ee674f84aff40da64f9886879cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181177"
---
# <a name="active-directory-service-interfaces-objects"></a>Objetos de interfaces de serviço do Active Directory

O modelo de objeto ADSI consiste em objetos COM. Os clientes manipulam objetos com interfaces. Os provedores ADSI implementam os objetos e suas interfaces.

Objetos ADSI são objetos COM que representam um item em um serviço de diretório: computadores, usuários, arquivos, servidores, impressoras, filas de impressão e assim por diante; ou seja, elementos com os que os administradores de rede trabalham diariamente. A ADSI define diferentes tipos de objetos para representar diferentes tipos de elementos. Cada objeto, conforme mostrado na figura a seguir, dá suporte a uma ou mais interfaces COM que permitem o acesso a dados de objeto, geralmente chamados de metadados.

![objetos de interfaces de serviço do Active Directory](images/ds2objex.png)

Como as interfaces COM são conjuntos de propriedades e métodos logicamente conectados, você pode pensar em cada interface como um identificador para o objeto que fornece acesso a apenas um conjunto de funções lógicas por vez. A tabela a seguir lista os elementos ADSI fundamentais.



| Interface            | Descrição                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iads**             | Usado para identificação de objeto. Como a interface fundamental necessária em todos os objetos ADSI, os [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) fornece acesso aos metadados de objeto, incluindo sua definição no esquema ADSI. Os IADs também fornece acesso às propriedades e métodos que gerenciam dados de objeto no cache de propriedades.                                                                                   |
| **IADsContainer**    | Usado para gerenciamento e detecção de objetos. Todos os objetos de contêiner ADSI exigem a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para gerenciar a criação, exclusão, cópia e movimentação de objetos, associação e enumeração.                                                                                                                                                                      |
| **IADsPropertyList** | Usado para gerenciamento de propriedade de objeto. A [**interface IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) otimiza o gerenciamento de dados de objeto no cache de propriedades.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Usado para acesso direto ao objeto. A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornece acesso a objetos de baixo nível para clientes que não usam Automação. Essa interface ignora o cache de propriedade do objeto e fornece acesso direto às propriedades do objeto. Para obter mais informações, [consulte As interfaces IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). |
| **IUnknown**         | Usado para gerenciamento de objetos COM. A [**interface IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) é necessária para todos os objetos COM.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Usado para dados de biblioteca de tipos e invocação de método. A [**interface IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) é necessária para todos os objetos de Automação.                                                                                                                                                                                                                             |



 

Objetos ADSI mais complexos podem expor interfaces adicionais. Por exemplo, [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) dá suporte a métodos que gerenciam coleções de elementos de diretório do mesmo tipo de dados. [**Os métodos IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) gerenciam as coleções de casos especiais de objetos que suportam a interface [**IADsMembers.**](/windows/desktop/api/Iads/nn-iads-iadsmembers) Para provedores que o suportam, a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) dá suporte a métodos para consultar serviços de diretório. Além disso, a ADSI fornece interfaces que representam itens lógicos e físicos conhecidos. Por exemplo, os objetos ADSI que representam os usuários são suportados por [**IADsUser,**](/windows/desktop/api/Iads/nn-iads-iadsuser)aqueles que representam computadores que suportam [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)e assim por diante. Para obter mais informações sobre objetos ADSI, consulte [As interfaces IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). Nem todos os provedores implementam todas as interfaces ou todos os métodos e propriedades em todas as interfaces. Para obter mais informações, consulte [Referência adsi](adsi-reference.md).

 

 