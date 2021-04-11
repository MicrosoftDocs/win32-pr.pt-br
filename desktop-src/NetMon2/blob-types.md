---
description: O Monitor de Rede usa três tipos de BLOBs (objetos binários grandes) para selecionar e conectar placas de interface de rede (NICs), capturar dados e manipular dados de NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Tipos de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171822"
---
# <a name="blob-types"></a><span data-ttu-id="8911e-103">Tipos de BLOB</span><span class="sxs-lookup"><span data-stu-id="8911e-103">BLOB Types</span></span>

<span data-ttu-id="8911e-104">O Monitor de Rede usa três tipos de BLOBs (objetos binários grandes) para selecionar e conectar placas de interface de rede (NICs), capturar dados e manipular dados de NPP.</span><span class="sxs-lookup"><span data-stu-id="8911e-104">Network Monitor uses three types of binary large objects (BLOBs) to select and connect network interface cards (NICs), capture data, and manipulate NPP data.</span></span>

## <a name="npp-blob"></a><span data-ttu-id="8911e-105">BLOB NPP</span><span class="sxs-lookup"><span data-stu-id="8911e-105">NPP BLOB</span></span>

<span data-ttu-id="8911e-106">Os aplicativos usam BLOBs NPP para se conectar a uma NIC específica por meio de um NPP.</span><span class="sxs-lookup"><span data-stu-id="8911e-106">Applications use NPP BLOBs to connect to a specific NIC through an NPP.</span></span> <span data-ttu-id="8911e-107">(O aplicativo faz a conexão com uma chamada para **CreateNPPInterface** e dados de localização no blob NPP.) Um aplicativo também pode armazenar seus dados de configuração no BLOB NPP para configurar o NPP.</span><span class="sxs-lookup"><span data-stu-id="8911e-107">(The application makes the connection with a call to **CreateNPPInterface** and location data in the NPP BLOB.) An application can also store its configuration data in the NPP BLOB to configure the NPP.</span></span> <span data-ttu-id="8911e-108">Além disso, um aplicativo que salva seu BLOB NPP não é necessário para percorrer o localizador para reutilizar esse BLOB.</span><span class="sxs-lookup"><span data-stu-id="8911e-108">Also, an application that saves its NPP BLOB is not required to go through the Finder to reuse that BLOB.</span></span>

## <a name="filter-blob"></a><span data-ttu-id="8911e-109">BLOB de filtro</span><span class="sxs-lookup"><span data-stu-id="8911e-109">Filter BLOB</span></span>

<span data-ttu-id="8911e-110">Um BLOB de filtro contém critérios definidos pelo aplicativo que você pode usar para selecionar um NPP e uma NIC.</span><span class="sxs-lookup"><span data-stu-id="8911e-110">A filter BLOB contains application-defined criteria that you can use to select an NPP and a NIC.</span></span> <span data-ttu-id="8911e-111">Por exemplo, um aplicativo pode solicitar uma NIC específica, somente placas Ethernet ou cartões que dão suporte a uma taxa de captura de quadro específica.</span><span class="sxs-lookup"><span data-stu-id="8911e-111">For example, an application can request a specific NIC, only Ethernet cards, or cards that support a specific frame capture rate.</span></span>

## <a name="special-blob"></a><span data-ttu-id="8911e-112">BLOB especial</span><span class="sxs-lookup"><span data-stu-id="8911e-112">Special BLOB</span></span>

<span data-ttu-id="8911e-113">Quando um NPP requer dados adicionais antes de poder retornar um BLOB NPP a um aplicativo, o NPP usa um BLOB especial.</span><span class="sxs-lookup"><span data-stu-id="8911e-113">When an NPP requires additional data before it can return an NPP BLOB to an application, the NPP uses a special BLOB.</span></span> <span data-ttu-id="8911e-114">Geralmente, o aplicativo não precisará ou usará BLOBs especiais para que eles não sejam retornados a um aplicativo, a menos que um sinalizador específico seja definido em uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="8911e-114">Most often, the application will not need or use special BLOBs so they are not returned to an application unless a specific flag is set in one function call.</span></span> <span data-ttu-id="8911e-115">Por exemplo, um NPP remoto usa um BLOB especial porque um nome de caminho é necessário para estabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="8911e-115">For example, a remote NPP uses a special BLOB because a path name is required to make a connection.</span></span> <span data-ttu-id="8911e-116">Um aplicativo que recebe um BLOB especial de NPP remoto pode adicionar a cadeia de caracteres e chamar de volta para o localizador para obter uma tabela de BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="8911e-116">An application that receives a remote NPP special BLOB could add the string and call back into the Finder to get an NPP BLOB table.</span></span> <span data-ttu-id="8911e-117">Para obter mais informações, consulte [entradas de blob especiais](special-blob-entries.md).</span><span class="sxs-lookup"><span data-stu-id="8911e-117">For more information, see [Special BLOB Entries](special-blob-entries.md).</span></span>

 

 



