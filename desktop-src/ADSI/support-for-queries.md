---
title: Suporte para consultas
description: Ao implementar a interface IDirectorySearch, os provedores ADSI têm acesso a um subconjunto de OLE DB recursos somente leitura.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Suporte para ADSI de consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ad1892cf7c0e619ef55b9c3e5af6885d4cbdc7ac68fbcbd206524128b283d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023223"
---
# <a name="support-for-queries"></a>Suporte para consultas

Ao implementar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , os provedores ADSI têm acesso a um subconjunto de OLE DB recursos somente leitura.

A implementação de ADSI dos métodos do [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) em si usa as interfaces OLE DB descritas na ADSI versão 1,0, incluindo a seguinte lista de objetos com:

-   Objeto de fonte de dados (o serviço de diretório), com suporte para **IDBInitialize**, **IDBCreateSession**, **IDBProperties** e **IPersist**.
-   Objeto DBSessions, com suporte para **IOpenRowSet**, **ISessionProperties** e **ICreateCommand**.
-   Objeto Command, com suporte a **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** e **IConvertType**.
-   Objeto Rowset, com suporte a **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.

Para obter mais informações sobre OLE DB, consulte a referência do programador de OLE DB no SDK (Software Development Kit) da plataforma.

 

 




