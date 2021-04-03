---
description: Para forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM, crie o pacote de instalação do aplicativo para especificar uma relação de componentes isolados entre o servidor e o cliente.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Instalando um componente não COM em um local privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837319"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a><span data-ttu-id="8d7dc-103">Instalando um componente não COM em um local privado</span><span class="sxs-lookup"><span data-stu-id="8d7dc-103">Installing a non-COM Component to a Private Location</span></span>

<span data-ttu-id="8d7dc-104">Para forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM, crie o pacote de instalação do aplicativo para especificar uma relação de [componentes isolados](isolated-components.md) entre o servidor e o cliente.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-104">To force a client application to always use the same copy of a non-COM server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="8d7dc-105">Isso instala uma cópia privada do componente de servidor em um local usado exclusivamente pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="8d7dc-106">Faça o seguinte ao criar o pacote:</span><span class="sxs-lookup"><span data-stu-id="8d7dc-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="8d7dc-107">Coloque a DLL do servidor e o cliente. exe em componentes separados.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="8d7dc-108">Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente cliente na \_ coluna compartilhada do componente e o aplicativo cliente na \_ coluna aplicativo do componente.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="8d7dc-109">Inclua a [ação IsolateComponents](isolatecomponents-action.md) nas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="8d7dc-110">Defina o bit msidbComponentAttributesSharedDllRefCount no registro da [tabela de componentes](component-table.md) para componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="8d7dc-111">O instalador requer esse Refcount global no local compartilhado para proteger os arquivos compartilhados e o registro nos casos em que há compartilhamento com outras tecnologias de instalação.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>
-   <span data-ttu-id="8d7dc-112">Evite criar um caminho registrado compartilhado entre componentes.</span><span class="sxs-lookup"><span data-stu-id="8d7dc-112">Avoid authoring a shared registered path across components.</span></span>

 

 



