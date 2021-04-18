---
description: Os leitores são dispositivos padrão em um sistema de cartão inteligente. Eles são controlados por meio de drivers e são introduzidos e removidos do sistema por meio de Plug and Play ou por meio do item dispositivos do painel de controle.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Leitores de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748958"
---
# <a name="smart-card-readers"></a><span data-ttu-id="ad451-104">Leitores de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="ad451-104">Smart Card Readers</span></span>

<span data-ttu-id="ad451-105">Os leitores são dispositivos padrão em um sistema de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ad451-105">Readers are standard devices in a [*smart card*](../secgloss/s-gly.md) system.</span></span> <span data-ttu-id="ad451-106">Eles são controlados por meio de drivers e são introduzidos e removidos do sistema por meio de Plug and Play ou por meio do item dispositivos do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="ad451-106">They are controlled through drivers, and are introduced to and removed from the system through Plug and Play or through the Control Panel Devices item.</span></span>

<span data-ttu-id="ad451-107">Cada leitor deve ser definido para ser usado pelo [*subsistema de cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ad451-107">Each reader must be defined for use by the [*smart card subsystem*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="ad451-108">O subsistema não é responsável por nenhum leitor especificamente fornecido a ele.</span><span class="sxs-lookup"><span data-stu-id="ad451-108">The subsystem is not responsible for any reader not specifically given to it.</span></span>

<span data-ttu-id="ad451-109">Os leitores de cartão inteligente podem ser divididos em grupos lógicos chamados grupos de leitores.</span><span class="sxs-lookup"><span data-stu-id="ad451-109">Smart card readers can be divided into logical groups called reader groups.</span></span> <span data-ttu-id="ad451-110">Esses grupos podem ser definidos pelo subsistema, bem como definidos por administradores e usuários.</span><span class="sxs-lookup"><span data-stu-id="ad451-110">These groups can be defined by the subsystem, as well as defined by administrators and users.</span></span> <span data-ttu-id="ad451-111">Um leitor pode pertencer a mais de um grupo de leitores</span><span class="sxs-lookup"><span data-stu-id="ad451-111">A reader can belong to more than one reader group</span></span>

<span data-ttu-id="ad451-112">O subsistema de cartão inteligente define os grupos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad451-112">The smart card subsystem defines the following groups.</span></span>



| <span data-ttu-id="ad451-113">Grupo</span><span class="sxs-lookup"><span data-stu-id="ad451-113">Group</span></span>                | <span data-ttu-id="ad451-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad451-114">Description</span></span>                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad451-115">Scartar $ webreaders</span><span class="sxs-lookup"><span data-stu-id="ad451-115">SCard$AllReaders</span></span>     | <span data-ttu-id="ad451-116">Esse grupo contém todos os leitores do sistema.</span><span class="sxs-lookup"><span data-stu-id="ad451-116">This group contains all the readers in the system.</span></span> <span data-ttu-id="ad451-117">Um novo leitor fornecido ao subsistema de cartão inteligente é incluído automaticamente no grupo de leitores de todo o sistema, Scartar $ rowgroup.</span><span class="sxs-lookup"><span data-stu-id="ad451-117">A new reader given to the smart card subsystem is automatically included in the system-wide reader group, SCard$AllReaders.</span></span>                         |
| <span data-ttu-id="ad451-118">Scartar $ defaultreadrs</span><span class="sxs-lookup"><span data-stu-id="ad451-118">SCard$DefaultReaders</span></span> | <span data-ttu-id="ad451-119">Esse grupo padrão, um para cada [*terminal*](../secgloss/t-gly.md), contém todos os leitores atribuídos ao terminal que não estão reservados para uso específico.</span><span class="sxs-lookup"><span data-stu-id="ad451-119">This default group, one for each [*terminal*](../secgloss/t-gly.md), contains all the readers assigned to the terminal that are not reserved for specific use.</span></span> |



 

 

 
