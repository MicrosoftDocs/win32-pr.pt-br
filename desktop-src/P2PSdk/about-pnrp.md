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
# <a name="about-pnrp"></a>Sobre o PNRP

O provedor de Namespace PNRP (Peer Name Resolution Protocol) (NSP) é uma tecnologia de resolução de nomes sem servidor que permite que os nós descubram uns aos outros. O PNRP usa a API do provedor de namespace do Winsock 2.

O suporte a IPv6 é exigido pelo PNRP e é o único protocolo de Internet nativo para a API. No entanto, o PNRP pode resolver endereços IPv4 por meio das tecnologias de transição 6to4 ou [Teredo](/windows/desktop/Teredo/portal) . Os usuários do Windows XP com Service Pack 1 (SP1) devem baixar o [pacote de rede avançado](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) para habilitar o suporte a IPv6 exigido pelo PNRP.

> [!Note]  
> Os aplicativos que usam o PNRP em um ambiente com um firewall exigem grupos de exceções que abrangem a porta específica do aplicativo, bem como a porta "3540-UDP" para PNRP. Esses grupos de exceções devem ser habilitados sempre que o aplicativo estiver em execução.

 

Embora o PNRP 2,0 seja nativo para as plataformas Windows Vista e Windows Server 2008, os usuários do Windows XP devem baixar Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) para atualizar para o PNRP 2,0.

 

 
