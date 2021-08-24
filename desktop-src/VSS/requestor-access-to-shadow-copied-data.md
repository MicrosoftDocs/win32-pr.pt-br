---
description: Depois que a cópia de sombra for concluída, o mecanismo mais importante para obter acesso aos dados de arquivo que ele contém é por meio do uso do objeto de dispositivo da cópia de sombra.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Acesso do solicitante aos dados copiados de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779e3947adff28c8f3190026921c398677afc7efaa484903bf165250f41bc191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767696"
---
# <a name="requester-access-to-shadow-copied-data"></a>Acesso do solicitante aos dados copiados de sombra

Depois que a cópia de sombra for concluída, o mecanismo mais importante para obter acesso aos dados de arquivo que ele contém é por meio do uso do [*objeto de dispositivo*](vssgloss-d.md)da cópia de sombra.

O membro **m \_ pwszSnapshotDeviceObject** de uma estrutura de [**\_ \_ prop instantâneo do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) é uma cadeia de caracteres que contém um objeto de dispositivo de volume copiado por sombra. Um solicitante pode obter um objeto de **\_ \_ prop snapshot do VSS** do volume copiado por sombra se ele souber **a \_ ID do VSS** do volume (GUID de identificação) e passá-lo para [**IVssBackupComponents:: getinstantâneoproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Um solicitante também pode obter informações de propriedade de cópia de sombra usando o membro **obj. snap** da estrutura de [**\_ \_ prop do objeto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que é uma estrutura de [**\_ \_ prop instantâneo do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtida usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para iterar na lista de objetos retornados por uma chamada para [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

O objeto de dispositivo deve ser interpretado como a raiz de um volume copiado por sombra. Por esse motivo, o objeto de dispositivo não contém nenhuma barra invertida (" \\ ").

Os caminhos no volume copiado de sombra são obtidos pela substituição da raiz do caminho original pelo objeto de dispositivo. Por exemplo, dado um caminho no volume original de "C: \\ Database \\ \* . mdb" e uma instância [**de \_ \_ prop de instantâneo do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) de snapProp, você obteria o caminho no volume de sombra copiado concatenando snapPropm \_ pwszShadow copyDeviceObject, " \\ " e " \\ Database \\ \* . mdb".

Os conjuntos de arquivos do VSS podem ter caracteres curinga em seus descritores de arquivo, portanto, obter uma lista completa dos arquivos em uma cópia de sombra gerenciada por um componente pode exigir o uso de métodos como **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.

 

 



