---
description: Hot Sparing
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Hot Sparing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4d007e9219ea79ae3bda31be595c33b537661a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779583"
---
# <a name="hot-sparing"></a>Hot Sparing

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O Hot Sparing é a substituição de um disco ou unidade por um disco ou unidade com falha ou falhas. (Os provedores de hardware atuam nas unidades; os provedores de software agem em discos.) Você pode compartilhar uma unidade de hot spare entre todos os LUNs no subsistema ou associá-lo a um LUN específico. Da mesma forma, você pode associar um disco sobressalente a um único volume, pacote e provedor de software, ou compartilhá-lo entre todos os hosts em uma SAN.

Se o volume ou LUN associado for tolerante a falhas, você poderá substituir um hot spare por um disco ou unidade com falha e recompilar qualquer RAID ou espelho de paridade afetado. Você pode substituir um hot spare por um disco com falha, mesmo se o volume ou LUN associado não for tolerante a falhas. Supondo que você possa determinar a falha iminente antes da perda de dados catastrófica, você pode espelhar temporariamente o hot spare para o disco ou unidade com falha e, em seguida, remover o disco ou a unidade com falha.

O Hot Sparing pode ser automático ou manual. Se um provedor implementar o Hot Sparing automático, ele executará a substituição dinamicamente. O Hot Sparing manual exige a intervenção do operador ou do aplicativo. Um hot spare pode conter dados parciais ou formatação de um uso anterior. O VDS substitui o hot spare quando ocorre a substituição.

Você não pode usar um hot spare para operações de vinculação comuns. Se o hot spare for maior do que o disco ou a unidade com falha, qualquer espaço em excesso permanecerá não utilizado até que seja declarado explicitamente como disponível para associação. Depois que o hot spare for usado para recuperação, o disco ou a unidade não será mais um hot spare. Em outras palavras, o eixo de 1 16 GB não pode atuar como hot spares de 2 8 gigabytes.

 

 
