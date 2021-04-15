---
description: O Serviço de Cópias de Sombra de Volume (VSS) é um conjunto de APIs COM e C++ que permite que os backups de volume sejam executados enquanto os aplicativos no sistema (chamados gravadores) continuam a gravar nos volumes.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Referência da API de cópia de sombra de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501736"
---
# <a name="volume-shadow-copy-api-reference"></a><span data-ttu-id="d1a12-103">Referência da API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-103">Volume Shadow Copy API Reference</span></span>

<span data-ttu-id="d1a12-104">O Serviço de Cópias de Sombra de Volume (VSS) é um conjunto de APIs COM e C++ que permite que os backups de volume sejam executados enquanto os aplicativos no sistema (chamados gravadores) continuam a gravar nos volumes.</span><span class="sxs-lookup"><span data-stu-id="d1a12-104">The Volume Shadow Copy Service (VSS) is a set of COM and C++ APIs that enable volume backups to be performed while applications on the system (called writers) continue to write to the volumes.</span></span>

<span data-ttu-id="d1a12-105">O VSS dá suporte a esses backups por meio da criação de cópias de sombra, uma duplicata do volume original em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="d1a12-105">VSS supports these backups through the creation of shadow copies, a duplicate of the original volume at a given point in time.</span></span>

<span data-ttu-id="d1a12-106">Desenvolvedores de terceiros podem usar a API do VSS para criar solicitantes (como um aplicativo de backup) para criar e gerenciar cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="d1a12-106">Third-party developers can use the VSS API to create requesters (such as a backup application) to create and manage shadow copies.</span></span>

<span data-ttu-id="d1a12-107">O trabalho real de criar e representar cópias de sombra é conduzido por aplicativos de nível de sistema conhecidos como provedores.</span><span class="sxs-lookup"><span data-stu-id="d1a12-107">The actual work of creating and representing shadow copies is conducted by system-level applications known as providers.</span></span>

<span data-ttu-id="d1a12-108">Os desenvolvedores também podem usar a API para construir gravadores: aplicativos com reconhecimento de VSS capazes de coordenar operações de e/s com a criação e manipulação de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="d1a12-108">Developers can also use the API to construct writers: VSS-aware applications that are able to coordinate I/O operations with the creation and manipulation of shadow copies.</span></span>

-   [<span data-ttu-id="d1a12-109">Classes de API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-109">Volume Shadow Copy API Classes</span></span>](volume-shadow-copy-api-classes.md)
-   [<span data-ttu-id="d1a12-110">Tipos de dados da API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-110">Volume Shadow Copy API Data Types</span></span>](volume-shadow-copy-api-data-types.md)
-   [<span data-ttu-id="d1a12-111">Enumerações de API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-111">Volume Shadow Copy API Enumerations</span></span>](volume-shadow-copy-api-enumeration-types.md)
-   [<span data-ttu-id="d1a12-112">Funções da API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-112">Volume Shadow Copy API Functions</span></span>](volume-shadow-copy-api-functions.md)
-   [<span data-ttu-id="d1a12-113">Interfaces de API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-113">Volume Shadow Copy API Interfaces</span></span>](volume-shadow-copy-api-interfaces.md)
-   [<span data-ttu-id="d1a12-114">Estruturas de API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-114">Volume Shadow Copy API Structures</span></span>](volume-shadow-copy-api-structures.md)
-   [<span data-ttu-id="d1a12-115">Glossário de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="d1a12-115">Volume Shadow Copy Glossary</span></span>](volume-shadow-copy-glossary.md)

<span data-ttu-id="d1a12-116">Para obter mais informações sobre como escrever solicitantes e gravadores, consulte [usando o serviço de cópias de sombra de volume](using-the-volume-shadow-copy-service.md).</span><span class="sxs-lookup"><span data-stu-id="d1a12-116">For more information on writing requesters and writers, see [Using the Volume Shadow Copy Service](using-the-volume-shadow-copy-service.md).</span></span>

 

 



