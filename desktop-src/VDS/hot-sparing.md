---
description: Hot Sparing
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Hot Sparing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b8df9bc27e303277c869901872a9b879cb2d7df32764589501b9d33a51c3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125946"
---
# <a name="hot-sparing"></a>Hot Sparing

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O esparso quente é a substituição de um disco ou unidade para um disco ou unidade com falha ou falha. (Provedores de hardware atuam em unidades; provedores de software atuam em discos.) Você pode compartilhar uma unidade de sobressalente quente entre todos os LUNs no subsistema ou associá-la a um LUN específico. Da mesma forma, você pode associar um disco sobressalente a um único volume, pacote e provedor de software ou compartilhá-lo entre todos os hosts em uma SAN.

Se o volume ou LUN associado for tolerante a falhas, você poderá substituir um sobressalente por um disco ou unidade com falha e recriar qualquer RAID de paridade ou espelhos afetados. Você pode substituir um sobressalente quente por um disco com falha, mesmo que o volume ou LUN associado não seja tolerante a falhas. Supondo que você possa determinar a falha pendente antes da perda catastrófica de dados, você pode espelhar temporariamente o sobressalente quente para o disco ou unidade com falha e, em seguida, remover o disco ou a unidade com falha.

O espaçamento quente pode ser automático ou manual. Se um provedor implementar o esparso dinâmico automático, ele executará a substituição dinamicamente. O espaçamento a quente manual requer intervenção do operador ou do aplicativo. Um sobressalente quente pode conter dados parciais ou formatação de um uso anterior. O VDS substitui o sobressalente quente quando ocorre a substituição.

Não é possível usar um sobressalente quente para operações de associação comuns. Se o sobressalente quente for maior que o disco ou a unidade com falha, qualquer espaço em excesso permanecerá inutilizável até que seja declarado explicitamente disponível para associação. Depois que o sobressalente quente tiver sido usado para recuperação, o disco ou a unidade não será mais um sobressalente quente. Em outras palavras, um eixo de 16 gigabyte não pode atuar como dois sobressalente de 8 gigabyte.

 

 
