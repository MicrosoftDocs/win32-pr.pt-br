---
title: Suporte para consultas
description: Ao implementar a interface IDirectorySearch, os provedores ADSI têm acesso a um subconjunto de OLE DB recursos somente leitura.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Suporte para ADSI de consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748336"
---
# <a name="support-for-queries"></a>Suporte para consultas

Ao implementar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , os provedores ADSI têm acesso a um subconjunto de OLE DB recursos somente leitura.

A implementação de ADSI dos métodos do [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) em si usa as interfaces OLE DB descritas na ADSI versão 1,0, incluindo a seguinte lista de objetos com:

-   Objeto de fonte de dados (o serviço de diretório), com suporte para **IDBInitialize**, **IDBCreateSession**, **IDBProperties** e **IPersist**.
-   Objeto DBSessions, com suporte para **IOpenRowSet**, **ISessionProperties** e **ICreateCommand**.
-   Objeto Command, com suporte a **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** e **IConvertType**.
-   Objeto Rowset, com suporte a **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.

Para obter mais informações sobre OLE DB, consulte a referência do programador de OLE DB no SDK (Software Development Kit) da plataforma.

 

 




