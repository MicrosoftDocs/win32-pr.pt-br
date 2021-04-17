---
description: Um administrador pode forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM em um pacote existente&\# 8212; sem afetar outros aplicativos&\# 8212; especificando uma relação de componentes isolados entre o servidor e o cliente.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Tornar um componente não-COM em um pacote particular existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754356"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a><span data-ttu-id="240bf-103">Tornar um componente não-COM em um pacote particular existente</span><span class="sxs-lookup"><span data-stu-id="240bf-103">Make a non-COM Component in an Existing Package Private</span></span>

<span data-ttu-id="240bf-104">Um administrador pode forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM em um pacote existente, sem afetar outros aplicativos, especificando uma relação de [componentes isolados](isolated-components.md) entre o servidor e o cliente.</span><span class="sxs-lookup"><span data-stu-id="240bf-104">An administrator can force a client application to always use the same copy of a non-COM server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="240bf-105">Isso instala uma cópia privada do componente de servidor em um local usado exclusivamente pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="240bf-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="240bf-106">O administrador precisa usar transformações ou uma ferramenta de criação de pacote para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="240bf-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="240bf-107">Coloque a DLL do servidor e o cliente. exe em componentes separados.</span><span class="sxs-lookup"><span data-stu-id="240bf-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="240bf-108">Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente cliente na \_ coluna compartilhada do componente e o aplicativo cliente na \_ coluna aplicativo do componente.</span><span class="sxs-lookup"><span data-stu-id="240bf-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="240bf-109">Inclua a [ação IsolateComponents](isolatecomponents-action.md) nas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="240bf-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="240bf-110">Defina o bit **msidbComponentAttributesSharedDllRefCount** no registro da [tabela de componentes](component-table.md) para componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="240bf-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="240bf-111">O instalador requer esse Refcount global no local compartilhado para proteger os arquivos compartilhados e o registro nos casos em que há compartilhamento com outras tecnologias de instalação.</span><span class="sxs-lookup"><span data-stu-id="240bf-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



