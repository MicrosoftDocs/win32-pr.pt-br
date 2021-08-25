---
description: Empilhamento de configuração
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Empilhamento de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9018a2484ce4e5b9121d08abffee54911531b7f421cfef75643594e827fe350e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905548"
---
# <a name="configuration-stacking"></a>Empilhamento de configuração

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O empilhamento envolve a concatenação de um conjunto de mapeamentos de blocos lógicos. Você pode empilhar vários LUNs do mesmo subsistema em um LUN. Você pode empilhar um LUN junto com volumes do mesmo pacote em um volume. Além disso, você pode empilhar vários LUNs que são exibidos por subsistemas heterogêneos em um volume.

Como mostra a ilustração a seguir, a criação de um volume não altera a associação existente de um LUN colaborador. Da mesma forma, a desvinculação de um volume não Desassocia um LUN colaborador. A ilustração ilustra a configuração do RAID 0 1 (0 + 1). Essa configuração conhecida combina a distribuição (RAID 0) e o espelhamento (RAID 1), que emparelham o acesso rápido a dados do RAID 0 com a confiabilidade do RAID 1.

![Diagrama que mostra uma configuração RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

Os LUNs contribuintes podem ter tipos de ligação diferentes. Muitas configurações são possíveis com o VDS, mas são altamente improvável, como a próxima ilustração. Neste exemplo, um plex de volume é um LUN distribuído e o outro é um LUN espelhado de três vias.

![Diagrama que mostra uma configuração de VDS em que um plex de volume é um LUN distribuído e o outro é um LUN espelhado de 3 vias.](images/vdsstacklunvol.png)

Embora impraticável, este exemplo ilustra um aspecto importante do empilhamento. Como o Stack concatena os plexes, o VDS adiciona os três plexes de LUN aos dois plexes de volume para um total de cinco plexes.

 

 
