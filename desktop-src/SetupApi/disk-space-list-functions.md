---
description: As funções a seguir são usadas com a lista de espaço em disco.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Funções de lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e20e6f656110cc3b8c2ebd607f28b5d701ce3007b4ce8812f7e3bcad2f7f5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887362"
---
# <a name="disk-space-list-functions"></a>Funções de lista de Disk-Space

As funções a seguir são usadas com a lista de espaço em disco.



| Função                                                                                         | Descrição                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Ajusta a quantidade de espaço necessário para uma unidade especificada.                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Cria uma lista de espaço em disco e aloca recursos a ela.                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Destrói uma lista de espaço em disco, liberando os recursos alocados a ela.                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Duplica uma lista de espaço em disco como uma nova lista de espaço em disco independente.                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Preenche um buffer com as especificações de unidade para todas as unidades listadas na lista de espaço em disco.                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Retorna a quantidade total de espaço em disco necessária para concluir as operações de arquivo em uma unidade específica listada na lista de espaço em disco. |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Adiciona uma operação de cópia ou de exclusão de arquivo à lista de espaço em disco.                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Adiciona todas as operações de arquivo em uma seção **copiar arquivos** ou **Excluir arquivos** de um arquivo inf a uma lista de espaço em disco.                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Adiciona todas as operações de arquivo em uma seção de **instalação** de um arquivo inf à lista de espaço em disco.                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Remove uma operação de cópia ou de exclusão de arquivo de uma lista de espaço em disco.                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Remove todas as operações de arquivo em uma seção **copiar arquivos** ou **Excluir arquivos** de um arquivo inf de uma lista de espaço em disco.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Remove todas as operações de arquivo na seção de **instalação** de um arquivo INF da lista de espaço em disco.                                  |



 

 

 



