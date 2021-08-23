---
description: 'Você pode atribuir uma letra de unidade (por exemplo, X: \) para um volume local usando a função SetVolumeMountPoint, desde que não haja nenhum volume já atribuído a essa letra de unidade.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Atribuindo uma letra de unidade a um volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cc2e894580a394e73896291f05a2f54c615949bfeb63ea3e574deef1353d91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766216"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Atribuindo uma letra de unidade a um volume

Você pode atribuir uma letra de unidade (por exemplo, X: \) para um volume local usando a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , desde que não haja nenhum volume já atribuído a essa letra de unidade. Se o volume local já tiver uma letra de unidade. em seguida, [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) falhará. Para lidar com isso, primeiro exclua a letra da unidade usando a função [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) . Para obter um exemplo de código, consulte [editando as atribuições de letra da unidade](editing-drive-letter-assignments.md).

O sistema dá suporte a no máximo uma letra de unidade por volume. Portanto, você não pode ter C: \\ e F: \\ representar o mesmo volume.

> [!Caution]
>
> A exclusão de uma letra de unidade existente e a atribuição de uma nova pode interromper os caminhos existentes, como aqueles em atalhos de área de trabalho. Ele também pode quebrar o caminho para o programa que faz com que a letra da unidade seja alterada. com o gerenciamento de memória virtual Windows, isso pode interromper o aplicativo, deixando o sistema em um estado instável e possivelmente inutilizável. É responsabilidade do designer de programa evitar essas possíveis catástrofes.

 

 

 



