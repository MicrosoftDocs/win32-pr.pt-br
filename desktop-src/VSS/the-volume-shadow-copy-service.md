---
description: O Serviço de Cópias de Sombra de Volume (VSS) fornece a infraestrutura do sistema para executar aplicativos VSS em sistemas baseados no Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: O Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647175"
---
# <a name="the-volume-shadow-copy-service"></a><span data-ttu-id="35633-103">O Serviço de Cópias de Sombra de Volume</span><span class="sxs-lookup"><span data-stu-id="35633-103">The Volume Shadow Copy Service</span></span>

<span data-ttu-id="35633-104">O Serviço de Cópias de Sombra de Volume (VSS) fornece a infraestrutura do sistema para executar aplicativos VSS em sistemas baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="35633-104">The Volume Shadow Copy Service (VSS) provides the system infrastructure for running VSS applications on Windows-based systems.</span></span>

<span data-ttu-id="35633-105">Embora seja amplamente transparente para o usuário e o desenvolvedor, o VSS faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="35633-105">Though largely transparent to user and developer, VSS does the following:</span></span>

-   <span data-ttu-id="35633-106">Coordena atividades de provedores, gravadores e solicitantes na criação e no uso de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="35633-106">Coordinates activities of providers, writers, and requesters in the creation and use of shadow copies</span></span>
-   <span data-ttu-id="35633-107">Fornece o provedor de sistema padrão</span><span class="sxs-lookup"><span data-stu-id="35633-107">Furnishes the default system provider</span></span>
-   <span data-ttu-id="35633-108">Implementa a funcionalidade de driver de nível baixo necessária para que qualquer provedor funcione</span><span class="sxs-lookup"><span data-stu-id="35633-108">Implements low-level driver functionality necessary for any provider to work</span></span>

<span data-ttu-id="35633-109">O serviço VSS é iniciado sob demanda; portanto, para que as operações do VSS sejam bem-sucedidas, esse serviço precisa ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="35633-109">The VSS service starts on demand; therefore, for VSS operations to be successful, this service must be enabled.</span></span>

 

 



