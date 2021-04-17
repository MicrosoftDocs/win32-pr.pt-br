---
description: Antes de adicionar ou remover operações de arquivo da lista de espaço em disco, você deve criá-la usando a função SetupCreateDiskSpaceList.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Usando a lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769179"
---
# <a name="using-the-disk-space-list"></a>Usando a lista de Disk-Space

Antes de adicionar ou remover operações de arquivo da lista de espaço em disco, você deve criá-la usando a função [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .

Depois de criar uma lista de espaço em disco, você pode adicionar operações individuais de cópia de arquivo ou exclusão à lista usando [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista). Para adicionar todas as operações de cópia ou exclusão de arquivo em uma seção INF inteira, use a função [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) ou [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .

Depois de adicionar todas as operações de instalação à lista de espaço em disco, você pode consultá-las para descobrir quanto espaço em disco é necessário para a instalação especificada usando a função [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .

A função [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) retorna as especificações de unidade para cada unidade de destino referenciada nas operações de arquivo na lista de espaço em disco. Você pode usar essas informações para comparar programaticamente o espaço disponível nessas unidades com o espaço exigido pela instalação.

Para remover uma operação de arquivo da lista de espaço em disco, use a função [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) . Para remover todas as operações de cópia ou exclusão de arquivo de uma seção de INF inteira, use a função [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) ou [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .

Depois que a lista de espaço em disco não for mais necessária, você poderá liberar os recursos alocados a ela chamando a função [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .

 

 



