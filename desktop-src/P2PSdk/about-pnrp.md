---
description: O provedor de Namespace PNRP (Peer Name Resolution Protocol) (NSP) é uma tecnologia de resolução de nomes sem servidor que permite que os nós descubram uns aos outros.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Sobre o PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091647"
---
# <a name="about-pnrp"></a><span data-ttu-id="f1215-103">Sobre o PNRP</span><span class="sxs-lookup"><span data-stu-id="f1215-103">About PNRP</span></span>

<span data-ttu-id="f1215-104">O provedor de Namespace PNRP (Peer Name Resolution Protocol) (NSP) é uma tecnologia de resolução de nomes sem servidor que permite que os nós descubram uns aos outros.</span><span class="sxs-lookup"><span data-stu-id="f1215-104">The Peer Name Resolution Protocol (PNRP) Namespace Provider (NSP) is a serverless name resolution technology that allows nodes to discover each other.</span></span> <span data-ttu-id="f1215-105">O PNRP usa a API do provedor de namespace do Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="f1215-105">PNRP uses the Winsock 2 Namespace Provider API.</span></span>

<span data-ttu-id="f1215-106">O suporte a IPv6 é exigido pelo PNRP e é o único protocolo de Internet nativo para a API.</span><span class="sxs-lookup"><span data-stu-id="f1215-106">IPv6 support is required by PNRP and is the only Internet Protocol native to the API.</span></span> <span data-ttu-id="f1215-107">No entanto, o PNRP pode resolver endereços IPv4 por meio das tecnologias de transição 6to4 ou [Teredo](/windows/desktop/Teredo/portal) .</span><span class="sxs-lookup"><span data-stu-id="f1215-107">However, PNRP can resolve IPv4 addresses via the 6to4 or [Teredo](/windows/desktop/Teredo/portal) transition technologies.</span></span> <span data-ttu-id="f1215-108">Os usuários do Windows XP com Service Pack 1 (SP1) devem baixar o [pacote de rede avançado](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) para habilitar o suporte a IPv6 exigido pelo PNRP.</span><span class="sxs-lookup"><span data-stu-id="f1215-108">Windows XP with Service Pack 1 (SP1) users must download the [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) to enable the IPv6 support required by PNRP.</span></span>

> [!Note]  
> <span data-ttu-id="f1215-109">Os aplicativos que usam o PNRP em um ambiente com um firewall exigem grupos de exceções que abrangem a porta específica do aplicativo, bem como a porta "3540-UDP" para PNRP.</span><span class="sxs-lookup"><span data-stu-id="f1215-109">Applications using PNRP in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="f1215-110">Esses grupos de exceções devem ser habilitados sempre que o aplicativo estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="f1215-110">These exception groups should be enabled whenever the application is running.</span></span>

 

<span data-ttu-id="f1215-111">Embora o PNRP 2,0 seja nativo para as plataformas Windows Vista e Windows Server 2008, os usuários do Windows XP devem baixar Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) para atualizar para o PNRP 2,0.</span><span class="sxs-lookup"><span data-stu-id="f1215-111">While PNRP 2.0 is native to the Windows Vista and Windows Server 2008 platforms, Windows XP users must download Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) to upgrade to PNRP 2.0.</span></span>

 

 
