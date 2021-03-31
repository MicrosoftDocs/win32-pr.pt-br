---
title: Active Directory objetos de interfaces de serviço
description: O modelo de objeto ADSI consiste em objetos COM. Clientes manipulam objetos com interfaces. Os provedores ADSI implementam os objetos e suas interfaces.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- ADSI de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e356d9b1212b448d16bb6bba081f6141a877b0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823982"
---
# <a name="active-directory-service-interfaces-objects"></a>Active Directory objetos de interfaces de serviço

O modelo de objeto ADSI consiste em objetos COM. Clientes manipulam objetos com interfaces. Os provedores ADSI implementam os objetos e suas interfaces.

Os objetos ADSI são objetos COM que representam um item em um serviço de diretório: computadores, usuários, arquivos, servidores, impressoras, filas de impressão e assim por diante; ou seja, elementos que os administradores de rede trabalham com diariamente. A ADSI define diferentes tipos de objetos para representar diferentes tipos de elementos. Cada objeto, conforme mostrado na figura a seguir, dá suporte a uma ou mais interfaces COM que habilitam o acesso a dados de objeto, geralmente chamados de metadados.

![objetos de interfaces de serviço do Active Directory](images/ds2objex.png)

Como as interfaces COM são conjuntos de propriedades e métodos logicamente conectados, você pode considerar cada interface como um identificador para o objeto que fornece acesso a apenas um conjunto de funções lógicas de cada vez. A tabela a seguir lista os elementos fundamentais da ADSI.



| Interface            | Descrição                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IADs**             | Usado para identificação de objeto. Como a interface fundamental necessária em todos os objetos ADSI, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) fornece acesso a metadados de objeto, incluindo sua definição no esquema ADSI. IADs também fornece acesso às propriedades e aos métodos que gerenciam dados de objeto no cache de propriedades.                                                                                   |
| **IADsContainer**    | Usado para gerenciamento e detecção de objetos. Todos os objetos de contêiner ADSI exigem a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para gerenciar a criação, exclusão, cópia e movimentação de objetos, associação e enumeração.                                                                                                                                                                      |
| **IADsPropertyList** | Usado para gerenciamento de propriedade de objeto. A interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) otimiza o gerenciamento de dados de objeto no cache de propriedades.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Usado para acesso direto a objeto. A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornece acesso de objeto de baixo nível para clientes que não usam automação. Essa interface ignora o cache de propriedades do objeto e fornece acesso direto às propriedades do objeto. Para obter mais informações, consulte [as interfaces IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). |
| **IUnknown**         | Usado para gerenciamento de objetos COM. A interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) é necessária para todos os objetos com.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Usado para dados de biblioteca de tipos e invocação de método. A interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) é necessária para todos os objetos de automação.                                                                                                                                                                                                                             |



 

Objetos ADSI mais complexos podem expor interfaces adicionais. Por exemplo, [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) dá suporte a métodos que gerenciam coleções de elementos de diretório do mesmo tipo de dados. Os métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iadsgroup) gerenciam as coleções de casos especiais de objetos que dão suporte à interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) . Para provedores que dão suporte a ele, a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) dá suporte a métodos para consultar serviços de diretório. Além disso, a ADSI fornece interfaces que representam itens físicos e lógicos bem conhecidos. Por exemplo, os objetos ADSI que representam os usuários dão suporte a [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), aqueles que representam computadores que dão suporte a [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)e assim por diante. Para obter mais informações sobre objetos ADSI, consulte [as interfaces IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). Nem todos os provedores implementam todas as interfaces ou todos os métodos e propriedades em todas as interfaces. Para obter mais informações, consulte [referência ADSI](adsi-reference.md).

 

 