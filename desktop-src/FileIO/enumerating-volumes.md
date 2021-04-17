---
description: Para fazer uma lista completa dos volumes em um computador ou manipular cada volume por vez, você pode enumerar volumes.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Enumerando volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761733"
---
# <a name="enumerating-volumes"></a>Enumerando volumes

Para fazer uma lista completa dos volumes em um computador ou manipular cada volume por vez, você pode enumerar volumes. Em um volume, você pode [verificar se há pastas montadas](enumerating-volume-mount-points.md) ou outros objetos no volume.

Três funções permitem que um aplicativo enumere volumes em um computador:

-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

Essas três funções operam de maneira muito semelhante às funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Inicie uma pesquisa de volumes com [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew). Se a pesquisa for bem-sucedida, processe os resultados de acordo com o design do seu aplicativo. Em seguida, use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) em um loop para localizar e processar cada volume subsequente. Quando o fornecimento de volumes for esgotado, feche a pesquisa com [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).

Você não deve assumir nenhuma correlação entre a ordem dos volumes que são retornados por essas funções e a ordem dos volumes que são retornados por outras funções ou ferramentas. Em particular, não assuma nenhuma correlação entre a ordem de volume e as letras da unidade, conforme atribuído pelo BIOS (se houver) ou pelo administrador do disco.

Consulte [exemplos de pastas montadas](volume-mount-point-examples.md) para obter um exemplo de como enumerar os volumes em um computador.

 

 



