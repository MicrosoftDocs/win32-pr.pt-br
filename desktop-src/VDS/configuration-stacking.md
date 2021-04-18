---
description: Empilhamento de configuração
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Empilhamento de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104561762"
---
# <a name="configuration-stacking"></a>Empilhamento de configuração

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O empilhamento envolve a concatenação de um conjunto de mapeamentos de blocos lógicos. Você pode empilhar vários LUNs do mesmo subsistema em um LUN. Você pode empilhar um LUN junto com volumes do mesmo pacote em um volume. Além disso, você pode empilhar vários LUNs que são exibidos por subsistemas heterogêneos em um volume.

Como mostra a ilustração a seguir, a criação de um volume não altera a associação existente de um LUN colaborador. Da mesma forma, a desvinculação de um volume não Desassocia um LUN colaborador. A ilustração ilustra a configuração do RAID 0 1 (0 + 1). Essa configuração conhecida combina a distribuição (RAID 0) e o espelhamento (RAID 1), que emparelham o acesso rápido a dados do RAID 0 com a confiabilidade do RAID 1.

![Diagrama que mostra uma configuração RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

Os LUNs contribuintes podem ter tipos de ligação diferentes. Muitas configurações são possíveis com o VDS, mas são altamente improvável, como a próxima ilustração. Neste exemplo, um plex de volume é um LUN distribuído e o outro é um LUN espelhado de três vias.

![Diagrama que mostra uma configuração de VDS em que um plex de volume é um LUN distribuído e o outro é um LUN espelhado de 3 vias.](images/vdsstacklunvol.png)

Embora impraticável, este exemplo ilustra um aspecto importante do empilhamento. Como o Stack concatena os plexes, o VDS adiciona os três plexes de LUN aos dois plexes de volume para um total de cinco plexes.

 

 
