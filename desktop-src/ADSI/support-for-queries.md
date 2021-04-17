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
# <a name="support-for-queries"></a><span data-ttu-id="7f6fc-104">Suporte para consultas</span><span class="sxs-lookup"><span data-stu-id="7f6fc-104">Support for Queries</span></span>

<span data-ttu-id="7f6fc-105">Ao implementar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , os provedores ADSI têm acesso a um subconjunto de OLE DB recursos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7f6fc-105">By implementing the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, ADSI providers gain access to a subset of OLE DB read-only features.</span></span>

<span data-ttu-id="7f6fc-106">A implementação de ADSI dos métodos do [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) em si usa as interfaces OLE DB descritas na ADSI versão 1,0, incluindo a seguinte lista de objetos com:</span><span class="sxs-lookup"><span data-stu-id="7f6fc-106">The ADSI implementation of the methods of [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) itself uses the OLE DB interfaces described in ADSI Version 1.0, including the following list of COM objects:</span></span>

-   <span data-ttu-id="7f6fc-107">Objeto de fonte de dados (o serviço de diretório), com suporte para **IDBInitialize**, **IDBCreateSession**, **IDBProperties** e **IPersist**.</span><span class="sxs-lookup"><span data-stu-id="7f6fc-107">Data Source Object (the directory service), supporting **IDBInitialize**, **IDBCreateSession**, **IDBProperties**, and **IPersist**.</span></span>
-   <span data-ttu-id="7f6fc-108">Objeto DBSessions, com suporte para **IOpenRowSet**, **ISessionProperties** e **ICreateCommand**.</span><span class="sxs-lookup"><span data-stu-id="7f6fc-108">DBSessions Object, supporting **IOpenRowSet**, **ISessionProperties**, and **ICreateCommand**.</span></span>
-   <span data-ttu-id="7f6fc-109">Objeto Command, com suporte a **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** e **IConvertType**.</span><span class="sxs-lookup"><span data-stu-id="7f6fc-109">Command Object, supporting **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText**, and **IConvertType**.</span></span>
-   <span data-ttu-id="7f6fc-110">Objeto Rowset, com suporte a **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.</span><span class="sxs-lookup"><span data-stu-id="7f6fc-110">Rowset Object, supporting **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset**, and **IRowsetInfo**.</span></span>

<span data-ttu-id="7f6fc-111">Para obter mais informações sobre OLE DB, consulte a referência do programador de OLE DB no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="7f6fc-111">For more information about OLE DB, see the OLE DB Programmer's Reference in the Platform Software Development Kit (SDK).</span></span>

 

 




