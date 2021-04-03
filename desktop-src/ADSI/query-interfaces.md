---
title: Interfaces de consulta
description: Três tipos de interfaces ADSI podem ser usados para executar pesquisas de diretório. O ambiente de aplicativo e outros requisitos podem indicar qual interface é usada.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces de consulta
- Consultas ADSI, interfaces de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822190"
---
# <a name="query-interfaces"></a>Interfaces de consulta

Três tipos de interfaces ADSI podem ser usados para executar pesquisas de diretório. O ambiente de aplicativo e outros requisitos podem indicar qual interface é usada.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). O **IDirectorySearch** é uma interface com básica disponível apenas para programadores C/C++. Para obter mais informações, consulte [pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md).
-   Data. As interfaces ADO (ActiveX Data Object) são interfaces de automação que usam OLE DB. Use o ADO para consultas em aplicativos que dependem da automação. Isso inclui Visual Basic aplicativos, Active Server páginas e assim por diante. Para obter mais informações, consulte [pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB é um conjunto de interfaces C/C++ usado para consultar bancos de dados. Ao dar suporte a essas interfaces, os provedores ADSI podem implementar recursos de OLE DB avançados, como consultas distribuídas com outros provedores de OLE DB. Para obter mais informações, consulte [pesquisando com OLE DB](searching-with-ole-db.md).

 

 




