---
description: Para forçar um aplicativo de cliente COM sempre usar a mesma cópia de um servidor COM, crie o pacote de instalação do aplicativo para especificar uma relação de componentes isolados entre o servidor COM e o cliente.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Instalando um componente COM em um local privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827471"
---
# <a name="installing-a-com-component-to-a-private-location"></a><span data-ttu-id="e33e8-103">Instalando um componente COM em um local privado</span><span class="sxs-lookup"><span data-stu-id="e33e8-103">Installing a COM Component to a Private Location</span></span>

<span data-ttu-id="e33e8-104">Para forçar um aplicativo de cliente COM sempre usar a mesma cópia de um servidor COM, crie o pacote de instalação do aplicativo para especificar uma relação de [componentes isolados](isolated-components.md) entre o servidor com e o cliente.</span><span class="sxs-lookup"><span data-stu-id="e33e8-104">To force a COM-client application to always use the same copy of a COM-server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="e33e8-105">Isso instala uma cópia privada do componente COM-Server em um local usado exclusivamente pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="e33e8-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="e33e8-106">Faça o seguinte ao criar o pacote:</span><span class="sxs-lookup"><span data-stu-id="e33e8-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="e33e8-107">Coloque a DLL do servidor COM e o cliente. exe em componentes separados.</span><span class="sxs-lookup"><span data-stu-id="e33e8-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="e33e8-108">Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente com-Client na \_ coluna compartilhada do componente e o aplicativo cliente na \_ coluna aplicativo do componente.</span><span class="sxs-lookup"><span data-stu-id="e33e8-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="e33e8-109">Inclua a [ação IsolateComponents](isolatecomponents-action.md) nas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="e33e8-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="e33e8-110">Defina o bit msidbComponentAttributesSharedDllRefCount no registro da [tabela de componentes](component-table.md) para componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e33e8-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="e33e8-111">O instalador requer esse Refcount global no local compartilhado para proteger os arquivos compartilhados e o registro nos casos em que há compartilhamento com outras tecnologias de instalação.</span><span class="sxs-lookup"><span data-stu-id="e33e8-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



