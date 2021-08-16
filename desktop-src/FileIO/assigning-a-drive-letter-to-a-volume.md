---
description: 'Você pode atribuir uma letra da unidade (por exemplo, X: a um volume local usando a função SetVolumeMountPoint, desde que não haja nenhum volume já atribuído a essa letra da \) unidade.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Atribuindo uma letra da unidade a um volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cc2e894580a394e73896291f05a2f54c615949bfeb63ea3e574deef1353d91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766216"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Atribuindo uma letra da unidade a um volume

Você pode atribuir uma letra da unidade (por exemplo, X: a um volume local usando a função \) [**SetVolumeMountPoint,**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) desde que não haja nenhum volume já atribuído a essa letra da unidade. Se o volume local já tiver uma letra da unidade. Em [**seguida, SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) falhará. Para lidar com isso, primeiro exclua a letra da unidade usando a [**função DeleteVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) Para código de exemplo, consulte [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).

O sistema dá suporte a no máximo uma letra de unidade por volume. Portanto, você não pode ter C: \\ e F: \\ representam o mesmo volume.

> [!Caution]
>
> Excluir uma letra de unidade existente e atribuir um novo pode quebrar caminhos existentes, como aqueles em atalhos da área de trabalho. Ele também pode quebrar o caminho para o programa que está fazendo alterações na letra da unidade. Com Windows de memória virtual, isso pode quebrar o aplicativo, deixando o sistema em um estado instável e possivelmente inutilizável. É responsabilidade do designer do programa evitar essas possíveis catástrofes.

 

 

 



