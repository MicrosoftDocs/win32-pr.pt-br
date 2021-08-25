---
title: Interfaces de consulta
description: Três tipos de interfaces ADSI podem ser usados para executar pesquisas de diretório. O ambiente do aplicativo e outros requisitos podem indicar qual interface é usada.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces de consulta
- Consultas ADSI, interfaces de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967f111107549fd0e6352f0e93d3a747b287c040ea7d5e6cee48415aa7f7925f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637716"
---
# <a name="query-interfaces"></a>Interfaces de consulta

Três tipos de interfaces ADSI podem ser usados para executar pesquisas de diretório. O ambiente do aplicativo e outros requisitos podem indicar qual interface é usada.

-   [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) **IDirectorySearch** é uma interface COM básica disponível somente para programadores C/C++. Para obter mais informações, [consulte Pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md).
-   Ado. As interfaces ActiveX ADO (Objeto de Dados) são interfaces de Automação que usam OLE DB. Use o ADO para consultas em aplicativos que dependem da Automação. Isso inclui Visual Basic aplicativos, Active Server Pages e assim por diante. Para obter mais informações, consulte [Pesquisando com objetos ActiveX dados](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB é um conjunto de interfaces C/C++ usadas para consultar bancos de dados. Ao dar suporte a essas interfaces, os provedores ADSI podem implementar recursos OLE DB avançados, como consultas distribuídas com outros OLE DB provedores. Para obter mais informações, consulte [Pesquisando com OLE DB](searching-with-ole-db.md).

 

 




