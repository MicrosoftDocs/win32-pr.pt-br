---
title: protocolo PPP em conexões Ethernet
description: Os sistemas operacionais Windows Server 2003, Windows XP e posterior fornecem suporte para protocolo PPP over Ethernet (PPPoE). Para uma conexão PPPoE, defina os valores a seguir na estrutura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917604"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a><span data-ttu-id="04697-104">protocolo PPP em conexões Ethernet</span><span class="sxs-lookup"><span data-stu-id="04697-104">Point-to-Point Protocol over Ethernet Connections</span></span>

<span data-ttu-id="04697-105">Os sistemas operacionais Windows Server 2003, Windows XP e posterior fornecem suporte para protocolo PPP over Ethernet (PPPoE).</span><span class="sxs-lookup"><span data-stu-id="04697-105">Windows Server 2003, Windows XP, and later operating systems provide support for Point-to-Point Protocol over Ethernet (PPPoE).</span></span> <span data-ttu-id="04697-106">Para uma conexão PPPoE, defina os valores a seguir na estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="04697-106">For a PPPoE connection, set the following values in the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure.</span></span>



| <span data-ttu-id="04697-107">Membro</span><span class="sxs-lookup"><span data-stu-id="04697-107">Member</span></span>                      | <span data-ttu-id="04697-108">Valor</span><span class="sxs-lookup"><span data-stu-id="04697-108">Value</span></span>             |
|-----------------------------|-------------------|
| <span data-ttu-id="04697-109">RASENTRY.dwType</span><span class="sxs-lookup"><span data-stu-id="04697-109">RASENTRY.dwType</span></span>             | <span data-ttu-id="04697-110">\_Banda larga RASET</span><span class="sxs-lookup"><span data-stu-id="04697-110">RASET\_Broadband</span></span>  |
| <span data-ttu-id="04697-111">RAENTRY.szDeviceType</span><span class="sxs-lookup"><span data-stu-id="04697-111">RAENTRY.szDeviceType</span></span>        | <span data-ttu-id="04697-112">RASDT \_ PPPoE</span><span class="sxs-lookup"><span data-stu-id="04697-112">RASDT\_PPPoE</span></span>      |
| <span data-ttu-id="04697-113">RASENTRY.szLocalPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="04697-113">RASENTRY.szLocalPhoneNumber</span></span> | <span data-ttu-id="04697-114">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="04697-114">The service name.</span></span> |



 

<span data-ttu-id="04697-115">Use a função [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir esses valores.</span><span class="sxs-lookup"><span data-stu-id="04697-115">Use the [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) function to set these values.</span></span>

<span data-ttu-id="04697-116">Você também pode usar [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) e o \_ sinalizador RASEDFLAG NewBroadbandEntry para [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para exibir um assistente para a criação de uma entrada de lista telefônica PPPoE.</span><span class="sxs-lookup"><span data-stu-id="04697-116">You can also use [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) and the RASEDFLAG\_NewBroadbandEntry flag for [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) to display a wizard for creating a PPPoE phonebook entry.</span></span>

 

 